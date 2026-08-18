---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/using-threads.html"
breadcrumb-title: ''
description: 並列処理とパフォーマンスのために、Substance 3D Designer Pythonスクリプティングでスレッドを使用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using threads
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スレッドの使用
user-guide-description: ''
user-guide-title: ''
source-git-commit: e49409eb4835f6a6c9f17713511e07b7afa38028
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# スレッドの使用

プラグインは、Pythonのスレッド化モジュール&#x200B;*または* Qtを使用してPythonスレッド化関連のクラスを<b>作成</b>できます。

これは、Designerの実行中にバックグラウンド処理やI/O処理を行う場合に便利です。

Python APIをDesignerするのほとんどのクラスやメソッドは、<b>メインアプリケーションスレッド</b>から&#x200B;*のみ*&#x200B;呼び出すことができます。 そのため、Designerで現在開いているグラフに変更を加える場合は、メインアプリケーションスレッドから変更を加える必要があります。

考えられる解決策の1つは、次の例のように<b>QThread</b>と<b>キュー接続</b>を使用することです。

```
import time 

from PySide2 import QtCore 

 

 

## Our thread object.

class TimerThread(QtCore.QThread): 

    tick = QtCore.Signal() 

 

    def run(self): 

        for i in range(0, 7): 

            print("Emitting signal from thread %s" % QtCore.QThread.currentThread()) 

            self.tick.emit() 

            time.sleep(0.5) 

 

 

## Our receiver object, created on the main thread.

class Receiver(QtCore.QObject): 

    def __init__(self, parent=None): 

        super(Receiver, self).__init__(parent) 

 

    def onTick(self): 

## This is called on the main thread. It is safe to use the sd API here.

        print("Tick received in thread %s" % QtCore.QThread.currentThread()) 

 

 

timer = TimerThread() 

receiver = Receiver() 

 

## Use QtCore.Qt.QueuedConnection to make sure that slots are called on the main thread.

## You can also use QtCore.Qt.BlockingQueuedConnection if you need to block while the slot is called.

timer.tick.connect(receiver.onTick, QtCore.Qt.QueuedConnection) 

 

## Start out thread.

timer.start()
```
