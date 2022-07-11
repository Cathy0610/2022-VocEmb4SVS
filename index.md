<!-- ---
layout: default
---
 -->


# VocEmb4Sep: Boosting the Performance of Singing Voice Separation by Vocal Embeddings
### _Chenyi Li, Yi Li, Xuhao Du, Zhiyong Wu_

### Abstract
> Deep learning based methods have shown improved performance on singing voice separation (SVS). Most separation systems only pay attention to the separated sources while a few systems would consider auxiliary information. Aiming to separate cleaner vocals from the mixed music, we propose VocEmb4Sep to utilize vocal feature embeddings as auxiliary knowledge to condition the separation system and explore various ways to enhance the regulation effect of the embeddings on the SVS system. In this paper, firstly, a vocal feature encoder is trained to extract fine-grained vocal feature embeddings from pre-separated vocals. Secondly, an adaptation block is developed to integrate the embeddings into various separation networks. Finally, efficient training strategies are proposed to boost the conditional performance of the embeddings to the separation system. The experimental results demonstrate that our best strategy outperforms other separation systems on the MUSDB18 dataset with an SDR of 9.56 dB on vocals, establishing a new state-of-the-art for the separation of vocals.

---

## Introduction of the demo
Since we aim at reducing the distortion of vocals and interference of accompaniments, our demos demonstrate the improvement of _separator P_ applying **VocEmb4Sep** compared with the original _separator P_. In addition, we display the vocal extraction effects when there are sound effects in the music.  The demos of vocals separated by different methods classified according to their major effectiveness are listed below. These are some binaural music clips cut from [MUSDB18 dataset](https://sigsep.github.io/datasets/musdb.html#musdb18-compressed-stems). `VocEmb4Sep (Separator P)` means applying our proposed method **VocEmb4Sep** on _Separator P_ and `Reference` means the ground-truth vocals in the mixed music from the open datasets [MUSDB18 dataset](https://sigsep.github.io/datasets/musdb.html#musdb18-compressed-stems). 

> For brevity, we only show the spectrograms and waveforms of the **left channel**. To see the complete binaural spectrograms and waveforms, please click on `Expand binaural images`.

<!-- <html> -->
<!-- <style>
  th, tr, td {border: none!important; vertical-align: middle; padding: 0px; margin: 0px auto;};
  img {padding: 0px; border: 0px; margin: 0px;}
</style> -->


## Reducing the distortion of separated vocals

### Case 1
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix08s1.PNG'  alt='mix08s1' width='100%'></td>
        <td> <img src='./img/mix08wv1.PNG'  alt='mix08wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet08s1.PNG'  alt='res08s1' width='100%'></td>
        <td> <img src='./img/ResUNet08wv1.PNG'  alt='res08wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro08s1.PNG'  alt='pre08s1' width='100%'></td>
        <td> <img src='./img/preFro08wv1.PNG'  alt='pre08wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs08s1.PNG'  alt='hdemucs08s1' width='100%'></td>
        <td> <img src='./img/HDemucs08wv1.PNG'  alt='hdemucs08wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd08s1.PNG'  alt='hu08s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd08wv1.PNG'  alt='hu08wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean08s1.PNG'  alt='clean08s1' width='100%'></td>
        <td> <img src='./img/clean08wv1.PNG'  alt='clean08wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix08s2.PNG'  alt='mix08s2' width='100%'></td>
        <td> <img src='./img/mix08wv2.PNG'  alt='mix08wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet08s2.PNG'  alt='res08s2' width='100%'></td>
        <td> <img src='./img/ResUNet08wv2.PNG'  alt='res08wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro08s2.PNG'  alt='pre08s2' width='100%'></td>
        <td> <img src='./img/preFro08wv2.PNG'  alt='pre08wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs08s2.PNG'  alt='hdemucs08s2' width='100%'></td>
        <td> <img src='./img/HDemucs08wv2.PNG'  alt='hdemucs08wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd08s2.PNG'  alt='hu08s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd08wv2.PNG'  alt='hu08wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean08s2.PNG'  alt='clean08s2' width='100%'></td>
        <td> <img src='./img/clean08wv2.PNG'  alt='clean08wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
 
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/Mix_Shore_08.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/ResUNet_Shore_08.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/preFro_Shore_08.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/clean_Shore_08.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucs_Shore_08.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucsUpd2_Shore_08.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>
    

### Case 2
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix03s1.PNG'  alt='mix03s1' width='100%'></td>
        <td> <img src='./img/mix03wv1.PNG'  alt='mix03wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet03s1.PNG'  alt='res03s1' width='100%'></td>
        <td> <img src='./img/ResUNet03wv1.PNG'  alt='res03wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro03s1.PNG'  alt='pre03s1' width='100%'></td>
        <td> <img src='./img/preFro03wv1.PNG'  alt='pre03wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs03s1.PNG'  alt='hdemucs03s1' width='100%'></td>
        <td> <img src='./img/HDemucs03wv1.PNG'  alt='hdemucs03wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd03s1.PNG'  alt='hu03s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd03wv1.PNG'  alt='hu03wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean03s1.PNG'  alt='clean03s1' width='100%'></td>
        <td> <img src='./img/clean03wv1.PNG'  alt='clean03wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix03s2.PNG'  alt='mix03s2' width='100%'></td>
        <td> <img src='./img/mix03wv2.PNG'  alt='mix03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet03s2.PNG'  alt='res03s2' width='100%'></td>
        <td> <img src='./img/ResUNet03wv2.PNG'  alt='res03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro03s2.PNG'  alt='pre03s2' width='100%'></td>
        <td> <img src='./img/preFro03wv2.PNG'  alt='pre03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs03s2.PNG'  alt='hdemucs03s2' width='100%'></td>
        <td> <img src='./img/HDemucs03wv2.PNG'  alt='hdemucs03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd03s2.PNG'  alt='hu03s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd03wv2.PNG'  alt='hu03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean03s2.PNG'  alt='clean03s2' width='100%'></td>
        <td> <img src='./img/clean03wv2.PNG'  alt='clean03wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/Mix_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/ResUNet_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/preFro_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/clean_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucs_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucsUpd2_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>
    



## Reducing the interference of accompaniments

### Case 3
<div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix011s1.PNG'  alt='mix02s1' width='100%'></td>
        <td> <img src='./img/mix011wv1.PNG'  alt='mix02wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet011s1.PNG'  alt='res02s1' width='100%'></td>
        <td> <img src='./img/ResUNet011wv1.PNG'  alt='res02wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro011s1.PNG'  alt='pre02s1' width='100%'></td>
        <td> <img src='./img/preFro011wv1.PNG'  alt='pre02wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs011s1.PNG'  alt='hdemucs02s1' width='100%'></td>
        <td> <img src='./img/HDemucs011wv1.PNG'  alt='hdemucs02wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd011s1.PNG'  alt='hu02s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd011wv1.PNG'  alt='hu02wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean011s1.PNG'  alt='clean02s1' width='100%'></td>
        <td> <img src='./img/clean011wv1.PNG'  alt='clean02wv1' width='100%'></td>
    </tr>
 </table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix011s2.PNG'  alt='mix02s2' width='100%'></td>
        <td> <img src='./img/mix011wv2.PNG'  alt='mix02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet011s2.PNG'  alt='res02s2' width='100%'></td>
        <td> <img src='./img/ResUNet011wv2.PNG'  alt='res02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro011s2.PNG'  alt='pre02s2' width='100%'></td>
        <td> <img src='./img/preFro011wv2.PNG'  alt='pre02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs011s2.PNG'  alt='hdemucs02s2' width='100%'></td>
        <td> <img src='./img/HDemucs011wv2.PNG'  alt='hdemucs02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd011s2.PNG'  alt='hu02s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd011wv2.PNG'  alt='hu02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean011s2.PNG'  alt='clean02s2' width='100%'></td>
        <td> <img src='./img/clean011wv2.PNG'  alt='clean02wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/Mix_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/ResUNet_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/preFro_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/clean_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucs_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucsUpd2_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
  </table></div>
  

### Case 4
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix06s1.PNG'  alt='mix06s1' width='100%'></td>
        <td> <img src='./img/mix06wv1.PNG'  alt='mix06wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet06s1.PNG'  alt='res06s1' width='100%'></td>
        <td> <img src='./img/ResUNet06wv1.PNG'  alt='res06wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro06s1.PNG'  alt='pre06s1' width='100%'></td>
        <td> <img src='./img/preFro06wv1.PNG'  alt='pre06wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs06s1.PNG'  alt='hdemucs06s1' width='100%'></td>
        <td> <img src='./img/HDemucs06wv1.PNG'  alt='hdemucs06wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd06s1.PNG'  alt='hu06s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd06wv1.PNG'  alt='hu06wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean06s1.PNG'  alt='clean06s1' width='100%'></td>
        <td> <img src='./img/clean06wv1.PNG'  alt='clean06wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix06s2.PNG'  alt='mix06s2' width='100%'></td>
        <td> <img src='./img/mix06wv2.PNG'  alt='mix06wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet06s2.PNG'  alt='res06s2' width='100%'></td>
        <td> <img src='./img/ResUNet06wv2.PNG'  alt='res06wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro06s2.PNG'  alt='pre06s2' width='100%'></td>
        <td> <img src='./img/preFro06wv2.PNG'  alt='pre06wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs06s2.PNG'  alt='hdemucs06s2' width='100%'></td>
        <td> <img src='./img/HDemucs06wv2.PNG'  alt='hdemucs06wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd06s2.PNG'  alt='hu06s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd06wv2.PNG'  alt='hu06wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean06s2.PNG'  alt='clean06s2' width='100%'></td>
        <td> <img src='./img/clean06wv2.PNG'  alt='clean06wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
 
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/Mix_Bulldozer_06.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/ResUNet_Bulldozer_06.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/preFro_Bulldozer_06.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/clean_Bulldozer_06.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucs_Bulldozer_06.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucsUpd2_Bulldozer_06.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>

 
### Case 5

  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix07s1.PNG'  alt='mix07s1' width='100%'></td>
        <td> <img src='./img/mix07wv1.PNG'  alt='mix07wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet07s1.PNG'  alt='res07s1' width='100%'></td>
        <td> <img src='./img/ResUNet07wv1.PNG'  alt='res07wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro07s1.PNG'  alt='pre07s1' width='100%'></td>
        <td> <img src='./img/preFro07wv1.PNG'  alt='pre07wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs07s1.PNG'  alt='hdemucs07s1' width='100%'></td>
        <td> <img src='./img/HDemucs07wv1.PNG'  alt='hdemucs07wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd07s1.PNG'  alt='hu07s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd07wv1.PNG'  alt='hu07wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean07s1.PNG'  alt='clean07s1' width='100%'></td>
        <td> <img src='./img/clean07wv1.PNG'  alt='clean07wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix07s2.PNG'  alt='mix07s2' width='100%'></td>
        <td> <img src='./img/mix07wv2.PNG'  alt='mix07wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet07s2.PNG'  alt='res07s2' width='100%'></td>
        <td> <img src='./img/ResUNet07wv2.PNG'  alt='res07wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro07s2.PNG'  alt='pre07s2' width='100%'></td>
        <td> <img src='./img/preFro07wv2.PNG'  alt='pre07wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs07s2.PNG'  alt='hdemucs07s2' width='100%'></td>
        <td> <img src='./img/HDemucs07wv2.PNG'  alt='hdemucs07wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd07s2.PNG'  alt='hu07s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd07wv2.PNG'  alt='hu07wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean07s2.PNG'  alt='clean07s2' width='100%'></td>
        <td> <img src='./img/clean07wv2.PNG'  alt='clean07wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
 
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/Mix_Bulldozer_07.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/ResUNet_Bulldozer_07.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/preFro_Bulldozer_07.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/clean_Bulldozer_07.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucs_Bulldozer_07.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucsUpd2_Bulldozer_07.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>


### Case 6
<div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix012s1.PNG'  alt='mix01s1' width='100%'></td>
        <td> <img src='./img/mix012wv1.PNG'  alt='mix01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet012s1.PNG'  alt='res01s1' width='100%'></td>
        <td> <img src='./img/ResUNet012wv1.PNG'  alt='res01wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro012s1.PNG'  alt='pre01s1' width='100%'></td>
        <td> <img src='./img/preFro012wv1.PNG'  alt='pre01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs012s1.PNG'  alt='hdemucs01s1' width='100%'></td>
        <td> <img src='./img/HDemucs012wv1.PNG'  alt='hdemucs01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd012s1.PNG'  alt='hu01s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd012wv1.PNG'  alt='hu01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean012s1.PNG'  alt='clean01s1' width='100%'></td>
        <td> <img src='./img/clean012wv1.PNG'  alt='clean01wv1' width='100%'></td>
    </tr>
 </table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix012s2.PNG'  alt='mix01s2' width='100%'></td>
        <td> <img src='./img/mix012wv2.PNG'  alt='mix01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet012s2.PNG'  alt='res01s2' width='100%'></td>
        <td> <img src='./img/ResUNet012wv2.PNG'  alt='res01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro012s2.PNG'  alt='pre01s2' width='100%'></td>
        <td> <img src='./img/preFro012wv2.PNG'  alt='pre01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs012s2.PNG'  alt='hdemucs01s2' width='100%'></td>
        <td> <img src='./img/HDemucs012wv2.PNG'  alt='hdemucs01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd012s2.PNG'  alt='hu01s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd012wv2.PNG'  alt='hu01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean012s2.PNG'  alt='clean01s2' width='100%'></td>
        <td> <img src='./img/clean012wv2.PNG'  alt='clean01wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/mix_Angels_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/ResUNet_Angels_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/preFro_Angels_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>        
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/clean_Angels_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucs_Angels_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucsUpd_Angels_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
  </table></div>  
    
## Extract clean vocals from scenes with sound effects
In this part, we list music clips with sound effects. The results show that the separation systems can separate clean vocals with the sound effects reduced.

### Case 7
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix11s1.PNG'  alt='mix11s1' width='100%'></td>
        <td> <img src='./img/mix11wv1.PNG'  alt='mix11wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet11s1.PNG'  alt='res11s1' width='100%'></td>
        <td> <img src='./img/ResUNet11wv1.PNG'  alt='res11wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro11s1.PNG'  alt='pre11s1' width='100%'></td>
        <td> <img src='./img/preFro11wv1.PNG'  alt='pre11wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs11s1.PNG'  alt='hdemucs11s1' width='100%'></td>
        <td> <img src='./img/HDemucs11wv1.PNG'  alt='hdemucs11wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd11s1.PNG'  alt='hu11s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd11wv1.PNG'  alt='hu11wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean11s1.PNG'  alt='clean11s1' width='100%'></td>
        <td> <img src='./img/clean11wv1.PNG'  alt='clean11wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix11s2.PNG'  alt='mix11s2' width='100%'></td>
        <td> <img src='./img/mix11wv2.PNG'  alt='mix11wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet11s2.PNG'  alt='res11s2' width='100%'></td>
        <td> <img src='./img/ResUNet11wv2.PNG'  alt='res11wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro11s2.PNG'  alt='pre11s2' width='100%'></td>
        <td> <img src='./img/preFro11wv2.PNG'  alt='pre11wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs11s2.PNG'  alt='hdemucs11s2' width='100%'></td>
        <td> <img src='./img/HDemucs11wv2.PNG'  alt='hdemucs11wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd11s2.PNG'  alt='hu11s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd11wv2.PNG'  alt='hu11wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean11s2.PNG'  alt='clean11s2' width='100%'></td>
        <td> <img src='./img/clean11wv2.PNG'  alt='clean11wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
 
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/Mix_Actor_11.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/ResUNet_Actor_11.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/preFro_Actor_11.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/clean_Actor_11.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucs_Actor_11.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucsUpd2_Actor_11.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>

  
  
### Case 8
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix12s1.PNG'  alt='mix12s1' width='100%'></td>
        <td> <img src='./img/mix12wv1.PNG'  alt='mix12wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet12s1.PNG'  alt='res12s1' width='100%'></td>
        <td> <img src='./img/ResUNet12wv1.PNG'  alt='res12wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro12s1.PNG'  alt='pre12s1' width='100%'></td>
        <td> <img src='./img/preFro12wv1.PNG'  alt='pre12wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs12s1.PNG'  alt='hdemucs12s1' width='100%'></td>
        <td> <img src='./img/HDemucs12wv1.PNG'  alt='hdemucs12wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd12s1.PNG'  alt='hu12s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd12wv1.PNG'  alt='hu12wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean12s1.PNG'  alt='clean12s1' width='100%'></td>
        <td> <img src='./img/clean12wv1.PNG'  alt='clean12wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix12s2.PNG'  alt='mix12s2' width='100%'></td>
        <td> <img src='./img/mix12wv2.PNG'  alt='mix12wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet12s2.PNG'  alt='res12s2' width='100%'></td>
        <td> <img src='./img/ResUNet12wv2.PNG'  alt='res12wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro12s2.PNG'  alt='pre12s2' width='100%'></td>
        <td> <img src='./img/preFro12wv2.PNG'  alt='pre12wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs12s2.PNG'  alt='hdemucs12s2' width='100%'></td>
        <td> <img src='./img/HDemucs12wv2.PNG'  alt='hdemucs12wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd12s2.PNG'  alt='hu12s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd12wv2.PNG'  alt='hu12wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean12s2.PNG'  alt='clean12s2' width='100%'></td>
        <td> <img src='./img/clean12wv2.PNG'  alt='clean12wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/Mix_Atrophy_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/ResUNet_Atrophy_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/preFro_Atrophy_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/clean_Atrophy_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucs_Atrophy_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucsUpd2_Atrophy_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>
  
  
### Case 9
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix05s1.PNG'  alt='mix05s1' width='100%'></td>
        <td> <img src='./img/mix05wv1.PNG'  alt='mix05wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet05s1-1.PNG'  alt='res05s1' width='100%'></td>
        <td> <img src='./img/ResUNet05wv1-1.PNG'  alt='res05wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro05s1.PNG'  alt='pre05s1' width='100%'></td>
        <td> <img src='./img/preFro05wv1.PNG'  alt='pre05wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs05s1.PNG'  alt='hdemucs05s1' width='100%'></td>
        <td> <img src='./img/HDemucs05wv1.PNG'  alt='hdemucs05wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd05s1.PNG'  alt='hu05s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd05wv1.PNG'  alt='hu05wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean05s1.PNG'  alt='clean05s1' width='100%'></td>
        <td> <img src='./img/clean05wv1.PNG'  alt='clean05wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix05s2.PNG'  alt='mix05s2' width='100%'></td>
        <td> <img src='./img/mix05wv2.PNG'  alt='mix05wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet05s2-1.PNG'  alt='res05s2' width='100%'></td>
        <td> <img src='./img/ResUNet05wv2-1.PNG'  alt='res05wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro05s2.PNG'  alt='pre05s2' width='100%'></td>
        <td> <img src='./img/preFro05wv2.PNG'  alt='pre05wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs05s2.PNG'  alt='hdemucs05s2' width='100%'></td>
        <td> <img src='./img/HDemucs05wv2.PNG'  alt='hdemucs05wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd05s2.PNG'  alt='hu05s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd05wv2.PNG'  alt='hu05wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean05s2.PNG'  alt='clean05s2' width='100%'></td>
        <td> <img src='./img/clean05wv2.PNG'  alt='clean05wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/mix_Moos_05.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/ResUNet_Moos_05-1.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/preFro_Moos_05.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/clean_Moos_05.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucs_Moos_05.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucsUpd_Moos_05.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>
 

### Case 10
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix04s1.PNG'  alt='mix04s1' width='100%'></td>
        <td> <img src='./img/mix04wv1.PNG'  alt='mix04wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet04s1.PNG'  alt='res04s1' width='100%'></td>
        <td> <img src='./img/ResUNet04wv1.PNG'  alt='res04wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro04s1.PNG'  alt='pre04s1' width='100%'></td>
        <td> <img src='./img/preFro04wv1.PNG'  alt='pre04wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs04s1.PNG'  alt='hdemucs04s1' width='100%'></td>
        <td> <img src='./img/HDemucs04wv1.PNG'  alt='hdemucs04wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd04s1.PNG'  alt='hu04s1' width='100%'></td>
        <td> <img src='./img/HDemucsUpd04wv1.PNG'  alt='hu04wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean04s1.PNG'  alt='clean04s1' width='100%'></td>
        <td> <img src='./img/clean04wv1.PNG'  alt='clean04wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./img/mix04s2.PNG'  alt='mix04s2' width='100%'></td>
        <td> <img src='./img/mix04wv2.PNG'  alt='mix04wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./img/ResUNet04s2.PNG'  alt='res04s2' width='100%'></td>
        <td> <img src='./img/ResUNet04wv2.PNG'  alt='res04wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./img/preFro04s2.PNG'  alt='pre04s2' width='100%'></td>
        <td> <img src='./img/preFro04wv2.PNG'  alt='pre04wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./img/HDemucs04s2.PNG'  alt='hdemucs04s2' width='100%'></td>
        <td> <img src='./img/HDemucs04wv2.PNG'  alt='hdemucs04wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./img/HDemucsUpd04s2.PNG'  alt='hu04s2' width='100%'></td>
        <td> <img src='./img/HDemucsUpd04wv2.PNG'  alt='hu04wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Reference</b> </td>
        <td> <img src='./img/clean04s2.PNG'  alt='clean04s2' width='100%'></td>
        <td> <img src='./img/clean04wv2.PNG'  alt='clean04wv2' width='100%'></td>
    </tr>
</table>
</details>
<br/>
<table style="margin-left: auto; margin-right: auto; align:center; border: none!important; width: 100%">
    <tr>
        <td align='center'>Mixture</td>
        <td align='center'>ResUNetDecouple+</td>
        <td align='center'>VocEmb4Sep (ResUNetDecouple+)</td>
    </tr>
    <tr>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/mix_OHNO_04.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/ResUNet_OHNO_04.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./data/preFro_OHNO_04.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>Reference</td>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/clean_OHNO_04.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucs_OHNO_04.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./data/HDemucsUpd_OHNO_04.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>
  
