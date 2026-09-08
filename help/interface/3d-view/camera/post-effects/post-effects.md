---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/interface/3d-view/camera/post-effects.html"
breadcrumb-title: ''
description: 3Dビューカメラに後処理効果を適用して、マテリアルのプレビューと表示を強化します。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D view > Camera > Post effects
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ポストエフェクト
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 4%

---


# ポストエフェクト

![ポストエフェクト](../../../../assets/postEffects.png "ポストエフェクト"){zoomable="yes"}

カメラのプロパティで、ポストエフェクトを有効にしてレンダリングを強化したり、特定のマテリアルプロパティを確認したりできます。

これらの効果は社内で開発されており、ラスタライザーおよびGPU パストレーサー [レンダラー](../../../../interface/3d-view/3d-renderers/3d-renderers.md)でのみ使用できます。

[3Dシーンリソース](../../../../resources/3d-scene-resource/3d-scene-resource.md)または[シーン状態ファイル](../../../../working-with-3d-scenes/working-with-3d-scenes.md)の保存時に有効にされたポストエフェクトは、シーン状態の一部として保存されます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## トーンマッピング

</td>
<td style="border: 0;" valign="top">

### ブルーム

</td>
<td style="border: 0;" valign="top">

### 被写界深度

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## トーンマッピング

特定のアルゴリズムやルックアップテーブル(LUT)に従って、レンダリングの色を再マップします。

これにより、アプリケーション間のカラーの一貫性を高めることができます。 例えば、AgXトーンマッパーはBlenderでも使用できます。

+++Reinhard


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXReinhard.jpg" alt="PostFXReinhard">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXReinhard](../../../../assets/PostFXReinhard.jpg "PostFXReinhard")

+++

+++Atan


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAtan.jpg" alt="PostFXAtan">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAtan](../../../../assets/PostFXAtan.jpg "PostFXAtan")

+++

+++Exp


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXExp.jpg" alt="PostFXExp">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXExp](../../../../assets/PostFXExp.jpg "PostFXExp")

+++

+++ログ


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXLog.jpg" alt="PostFXLog">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXLog](../../../../assets/PostFXLog.jpg "PostFXLog")

+++

+++Aces


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAces.jpg" alt="PostFXAces">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAces](../../../../assets/PostFXAces.jpg "PostFXAces")

+++

+++ヘイル


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXHejl.jpg" alt="PostFXHejl">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXHejl](../../../../assets/PostFXHejl.jpg "PostFXHejl")

+++

+++ニュートラル


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXNeutral.jpg" alt="PostFXNeutral">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXNeutral](../../../../assets/PostFXNeutral.jpg "PostFXNeutral")

+++

+++Agx


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXAgx.jpg" alt="PostFXAgx">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXAgx](../../../../assets/PostFXAgx.jpg "PostFXAgx")

+++

+++Pbrニュートラル


<table>
  <tr>
    <td>
      <img src="../../../../assets/PostFXDisabled.jpg" alt="PostFXDisabled">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/PostFXPbrNeutral.jpg" alt="PostFXPbrNeutral">
      <br><i>後</i>
    </td>
  </tr>
</table>



![PostFXDisabled](../../../../assets/PostFXDisabled.jpg "PostFXDisabled")

![PostFXPbrNeutral](../../../../assets/PostFXPbrNeutral.jpg "PostFXPbrNeutral")

+++

## ブルーム

非常に明るい領域から光量の少ない領域に向かって光が外に漏れ出すフリンジをカメラ内でシミュレートします。

この効果は、シーンの照明、カメラの露光量、および発光マテリアルの影響を受けます。

+++しきい値
この値を超えるとブルームが表示されるルミナンス値。

*左： 1.0 /右： 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomThreshold1.jpg" alt="bloomThreshold1">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/bloomThreshold4.jpg" alt="bloomThreshold4">
      <br><i>後</i>
    </td>
  </tr>
</table>



![bloomThreshold1](../../../../assets/bloomThreshold1.jpg "bloomThreshold1")

![bloomThreshold4](../../../../assets/bloomThreshold4.jpg "bloomThreshold4")

+++

+++減衰
ブルーム減衰ランプ。値が小さいほど、ブルームの半径が短くなります。

*左： 1.0 /右： 0.6*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomFalloff1.jpg" alt="bloomFalloff1">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/bloomFalloff0-6.jpg" alt="bloomFalloff0-6">
      <br><i>後</i>
    </td>
  </tr>
</table>



![bloomFalloff1](../../../../assets/bloomFalloff1.jpg "bloomFalloff1")

![bloomFalloff0-6](../../../../assets/bloomFalloff0-6.jpg "bloomFalloff0-6")

+++

+++レベル
花の咲き具合。 値を大きくすると、明るく鮮明な明るいフリンジになります。

*左： 8.0 /右： 2.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomLevel8.jpg" alt="bloomLevel8">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/bloomLevel2.jpg" alt="bloomLevel2">
      <br><i>後</i>
    </td>
  </tr>
</table>



![bloomLevel8](../../../../assets/bloomLevel8.jpg "bloomLevel8")

![bloomLevel2](../../../../assets/bloomLevel2.jpg "bloomLevel2")

+++

+++カラーシフト
花の影響を受ける領域の色相を暖色寄りにオフセットします。

*左： 0.0 /右： 0.8*



<table>
  <tr>
    <td>
      <img src="../../../../assets/bloomColorShift0.jpg" alt="bloomColorShift0">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/bloomColorShift0-8.jpg" alt="bloomColorShift0-8">
      <br><i>後</i>
    </td>
  </tr>
</table>



![bloomColorShift0](../../../../assets/bloomColorShift0.jpg "bloomColorShift0")

![bloomColorShift0-8](../../../../assets/bloomColorShift0-8.jpg "bloomColorShift0-8")

+++

## 被写界深度

焦点距離より近い物や遠い物がぼやける場合に、カメラレンズによって引き起こされる光学現象をシミュレートします。

このエフェクトは、カメラの「F-Stop」パラメーターと「Focus distance」パラメーターの両方の影響を受けます。

>[!TIP]
>
> カメラのピントをすばやく合わせるには、ピントを合わせるシーンの場所にカーソルを置き、Ctrl+LMB(Windows)またはCmd+LMB(macOS)を押して、その場所にピントを合わせます。

+++最大半径
ぼかし効果の最大半径です。

*左： 32.0 /右： 4.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius32.jpg" alt="depthOfFieldMaxRadius32">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldMaxRadius4.jpg" alt="depthOfFieldMaxRadius4">
      <br><i>後</i>
    </td>
  </tr>
</table>



![depthOfFieldMaxRadius32](../../../../assets/depthOfFieldMaxRadius32.jpg "depthOfFieldMaxRadius32")

![depthOfFieldMaxRadius4](../../../../assets/depthOfFieldMaxRadius4.jpg "depthOfFieldMaxRadius4")

+++

+++コンポジットの適用量
フォーカスから外側へのブラー効果の大きさを指定します。

*左： 0.2 /右： 0.05*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-2.jpg" alt="depthOfFieldCompositeStrength0-2">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldCompositeStrength0-05.jpg" alt="depthOfFieldCompositeStrength0-05">
      <br><i>後</i>
    </td>
  </tr>
</table>



![depthOfFieldCompositeStrength0-2](../../../../assets/depthOfFieldCompositeStrength0-2.jpg "depthOfFieldCompositeStrength0-2")

![depthOfFieldCompositeStrength0-05](../../../../assets/depthOfFieldCompositeStrength0-05.jpg "depthOfFieldCompositeStrength0-05")

+++

+++縦方向の収差
焦点距離から離れて発生する収差の強度。

「収差」は、異なる波長の光がわずかに異なる焦点距離を持つことをシミュレートします。その結果、色が相殺したように見え、焦点が微妙に異なります。

*左： 0.0 /ライト： 1.0*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration0.jpg" alt="depthOfFieldLaterialAberration0">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldLongitudinalAberration1.jpg" alt="depthOfFieldLongterialAberration1">
      <br><i>後</i>
    </td>
  </tr>
</table>



![depthOfFieldLongitualAberration0](../../../../assets/depthOfFieldLongitudinalAberration0.jpg "depthOfFieldLongitualAberration0")

![depthOfFieldLongitualAberration1](../../../../assets/depthOfFieldLongitudinalAberration1.jpg "depthOfFieldLongitualAberration1")

+++

+++無色収差
色収差を無彩色（一部またはすべての色が同じ焦点距離を持つことを意味）にするかどうかを指定します。

これにより、ぼかし効果がより均等に分布するように見えます。

*左： True /右： False*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationYes.jpg" alt="depthOfFieldAchromaticAberrationYes">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticAberrationNo.jpg" alt="depthOfFieldAchromaticAberrationNo">
      <br><i>後</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticAberrationYes](../../../../assets/depthOfFieldAchromaticAberrationYes.jpg "depthOfFieldAchromaticAberrationYes")

![depthOfFieldAchromaticAberrationNo](../../../../assets/depthOfFieldAchromaticAberrationNo.jpg "depthOfFieldAchromaticAberrationNo")

+++

+++口径食
シーン内で猫の目の効果を有効にします。斜めに入る光が円盤ではなく不規則な楕円に入り、ゆがみを引き起こす様子をシミュレートします。

この効果は絞り値が大きいほど、つまりF-Stop値が小さいほど顕著になります。

*左： True /右： False*



<table>
  <tr>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg" alt="depthOfFieldAchromaticCatsEyeYes">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg" alt="depthOfFieldAchromaticCatsEyeNo">
      <br><i>後</i>
    </td>
  </tr>
</table>



![depthOfFieldAchromaticCatsEyeYes](../../../../assets/depthOfFieldAchromaticCatsEyeYes.jpg "depthOfFieldAchromaticCatsEyeYes")

![depthOfFieldAchromaticCatsEyeNo](../../../../assets/depthOfFieldAchromaticCatsEyeNo.jpg "depthOfFieldAchromaticCatsEyeNo")

+++
