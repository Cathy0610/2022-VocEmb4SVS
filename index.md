---
layout: default
---



# Audio demo
For brevity, we only show the spectrograms and waveforms of the **right channel**. To see the complete binaural spectrograms and waveforms, please click on `Expand binaural images`.

<!-- <html> -->
<style>
  th, tr, td {border: none!important; vertical-align: middle; padding: 0px; margin: 0px auto;};
  img {padding: 0px; border: 0px; margin: 0px;}
</style>
  
## Case 1
<div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix01S1.PNG'  alt='mix01s1' width='100%'></td>
        <td> <img src='./fig/Mix01WV1.PNG'  alt='mix01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet01S1.PNG'  alt='res01s1' width='100%'></td>
        <td> <img src='./fig/ResUNet01WV1.PNG'  alt='res01wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro01S1.PNG'  alt='pre01s1' width='100%'></td>
        <td> <img src='./fig/preFro01WV1.PNG'  alt='pre01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs01S1.PNG'  alt='hdemucs01s1' width='100%'></td>
        <td> <img src='./fig/HDemucs01WV1.PNG'  alt='hdemucs01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd01S1.PNG'  alt='hu01s1' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd01WV1.PNG'  alt='hu01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean01S1.PNG'  alt='clean01s1' width='100%'></td>
        <td> <img src='./fig/clean01WV1.PNG'  alt='clean01wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix01S2.PNG'  alt='mix01s2' width='100%'></td>
        <td> <img src='./fig/Mix01WV2.PNG'  alt='mix01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet01S2.PNG'  alt='res01s2' width='100%'></td>
        <td> <img src='./fig/ResUNet01WV2.PNG'  alt='res01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro01S2.PNG'  alt='pre01s2' width='100%'></td>
        <td> <img src='./fig/preFro01WV2.PNG'  alt='pre01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs01S2.PNG'  alt='hdemucs01s2' width='100%'></td>
        <td> <img src='./fig/HDemucs01WV2.PNG'  alt='hdemucs01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd01S2.PNG'  alt='hu01s2' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd01WV2.PNG'  alt='hu01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean01S2.PNG'  alt='clean01s2' width='100%'></td>
        <td> <img src='./fig/clean01WV2.PNG'  alt='clean01wv2' width='100%'></td>
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
            <source src="./wav/Mix_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/ResUNet_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/preFro_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    <td align='center'>Clean</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucs_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucsUpd2_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/clean_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
  </table></div>
  
## Case 2  
<div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix02S1.PNG'  alt='mix02s1' width='100%'></td>
        <td> <img src='./fig/Mix02WV1.PNG'  alt='mix02wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet02S1.PNG'  alt='res02s1' width='100%'></td>
        <td> <img src='./fig/ResUNet02WV1.PNG'  alt='res02wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro02S1.PNG'  alt='pre02s1' width='100%'></td>
        <td> <img src='./fig/preFro02WV1.PNG'  alt='pre02wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs02S1.PNG'  alt='hdemucs02s1' width='100%'></td>
        <td> <img src='./fig/HDemucs02WV1.PNG'  alt='hdemucs02wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd02S1.PNG'  alt='hu02s1' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd02WV1.PNG'  alt='hu02wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean02S1.PNG'  alt='clean02s1' width='100%'></td>
        <td> <img src='./fig/clean02WV1.PNG'  alt='clean02wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix02S2.PNG'  alt='mix02s2' width='100%'></td>
        <td> <img src='./fig/Mix02WV2.PNG'  alt='mix02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet02S2.PNG'  alt='res02s2' width='100%'></td>
        <td> <img src='./fig/ResUNet02WV2.PNG'  alt='res02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro02S2.PNG'  alt='pre02s2' width='100%'></td>
        <td> <img src='./fig/preFro02WV2.PNG'  alt='pre02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs02S2.PNG'  alt='hdemucs02s2' width='100%'></td>
        <td> <img src='./fig/HDemucs02WV2.PNG'  alt='hdemucs02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd02S2.PNG'  alt='hu02s2' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd02WV2.PNG'  alt='hu02wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean02S2.PNG'  alt='clean02s2' width='100%'></td>
        <td> <img src='./fig/clean02WV2.PNG'  alt='clean02wv2' width='100%'></td>
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
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    <td align='center'>Clean</td>
    </tr>
    <tr>
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
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/clean_Atrophy_02.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
  </table></div>

## Case 3
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix03S1.PNG'  alt='mix03s1' width='100%'></td>
        <td> <img src='./fig/Mix03WV1.PNG'  alt='mix03wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet03S1.PNG'  alt='res03s1' width='100%'></td>
        <td> <img src='./fig/ResUNet03WV1.PNG'  alt='res03wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro03S1.PNG'  alt='pre03s1' width='100%'></td>
        <td> <img src='./fig/preFro03WV1.PNG'  alt='pre03wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs03S1.PNG'  alt='hdemucs03s1' width='100%'></td>
        <td> <img src='./fig/HDemucs03WV1.PNG'  alt='hdemucs03wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd03S1.PNG'  alt='hu03s1' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd03WV1.PNG'  alt='hu03wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean03S1.PNG'  alt='clean03s1' width='100%'></td>
        <td> <img src='./fig/clean03WV1.PNG'  alt='clean03wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix03S2.PNG'  alt='mix03s2' width='100%'></td>
        <td> <img src='./fig/Mix03WV2.PNG'  alt='mix03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet03S2.PNG'  alt='res03s2' width='100%'></td>
        <td> <img src='./fig/ResUNet03WV2.PNG'  alt='res03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro03S2.PNG'  alt='pre03s2' width='100%'></td>
        <td> <img src='./fig/preFro03WV2.PNG'  alt='pre03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs03S2.PNG'  alt='hdemucs03s2' width='100%'></td>
        <td> <img src='./fig/HDemucs03WV2.PNG'  alt='hdemucs03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd03S2.PNG'  alt='hu03s2' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd03WV2.PNG'  alt='hu03wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean03S2.PNG'  alt='clean03s2' width='100%'></td>
        <td> <img src='./fig/clean03WV2.PNG'  alt='clean03wv2' width='100%'></td>
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
            <source src="./wav/Mix_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/ResUNet_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/preFro_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    <td align='center'>Clean</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucs_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucsUpd2_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/clean_Atrophy_03.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>

## Case 4
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix04S1.PNG'  alt='mix04s1' width='100%'></td>
        <td> <img src='./fig/Mix04WV1.PNG'  alt='mix04wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet04S1.PNG'  alt='res04s1' width='100%'></td>
        <td> <img src='./fig/ResUNet04WV1.PNG'  alt='res04wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro04S1.PNG'  alt='pre04s1' width='100%'></td>
        <td> <img src='./fig/preFro04WV1.PNG'  alt='pre04wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs04S1.PNG'  alt='hdemucs04s1' width='100%'></td>
        <td> <img src='./fig/HDemucs04WV1.PNG'  alt='hdemucs04wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd04S1.PNG'  alt='hu04s1' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd04WV1.PNG'  alt='hu04wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean04S1.PNG'  alt='clean04s1' width='100%'></td>
        <td> <img src='./fig/clean04WV1.PNG'  alt='clean04wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix01S2.PNG'  alt='mix01s2' width='100%'></td>
        <td> <img src='./fig/Mix01WV2.PNG'  alt='mix01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet01S2.PNG'  alt='res01s2' width='100%'></td>
        <td> <img src='./fig/ResUNet01WV2.PNG'  alt='res01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro01S2.PNG'  alt='pre01s2' width='100%'></td>
        <td> <img src='./fig/preFro01WV2.PNG'  alt='pre01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs01S2.PNG'  alt='hdemucs01s2' width='100%'></td>
        <td> <img src='./fig/HDemucs01WV2.PNG'  alt='hdemucs01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd01S2.PNG'  alt='hu01s2' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd01WV2.PNG'  alt='hu01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean01S2.PNG'  alt='clean01s2' width='100%'></td>
        <td> <img src='./fig/clean01WV2.PNG'  alt='clean01wv2' width='100%'></td>
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
            <source src="./wav/Mix_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/ResUNet_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/preFro_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    <td align='center'>Clean</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucs_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucsUpd2_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/clean_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>
  
## Case 5
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix01S1.PNG'  alt='mix01s1' width='100%'></td>
        <td> <img src='./fig/Mix01WV1.PNG'  alt='mix01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet01S1.PNG'  alt='res01s1' width='100%'></td>
        <td> <img src='./fig/ResUNet01WV1.PNG'  alt='res01wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro01S1.PNG'  alt='pre01s1' width='100%'></td>
        <td> <img src='./fig/preFro01WV1.PNG'  alt='pre01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs01S1.PNG'  alt='hdemucs01s1' width='100%'></td>
        <td> <img src='./fig/HDemucs01WV1.PNG'  alt='hdemucs01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd01S1.PNG'  alt='hu01s1' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd01WV1.PNG'  alt='hu01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean01S1.PNG'  alt='clean01s1' width='100%'></td>
        <td> <img src='./fig/clean01WV1.PNG'  alt='clean01wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix01S2.PNG'  alt='mix01s2' width='100%'></td>
        <td> <img src='./fig/Mix01WV2.PNG'  alt='mix01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet01S2.PNG'  alt='res01s2' width='100%'></td>
        <td> <img src='./fig/ResUNet01WV2.PNG'  alt='res01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro01S2.PNG'  alt='pre01s2' width='100%'></td>
        <td> <img src='./fig/preFro01WV2.PNG'  alt='pre01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs01S2.PNG'  alt='hdemucs01s2' width='100%'></td>
        <td> <img src='./fig/HDemucs01WV2.PNG'  alt='hdemucs01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd01S2.PNG'  alt='hu01s2' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd01WV2.PNG'  alt='hu01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean01S2.PNG'  alt='clean01s2' width='100%'></td>
        <td> <img src='./fig/clean01WV2.PNG'  alt='clean01wv2' width='100%'></td>
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
            <source src="./wav/Mix_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/ResUNet_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/preFro_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    <td align='center'>Clean</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucs_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucsUpd2_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/clean_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>
  
## Case 6
  <div align='center'>
<table style="margin: 0,auto; align:center; vertical-align:middle; border: none!important">
    <tr>
        <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix01S1.PNG'  alt='mix01s1' width='100%'></td>
        <td> <img src='./fig/Mix01WV1.PNG'  alt='mix01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='middle'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet01S1.PNG'  alt='res01s1' width='100%'></td>
        <td> <img src='./fig/ResUNet01WV1.PNG'  alt='res01wv1' width='100%'></td>
    </tr>
    <tr>
        <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro01S1.PNG'  alt='pre01s1' width='100%'></td>
        <td> <img src='./fig/preFro01WV1.PNG'  alt='pre01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs01S1.PNG'  alt='hdemucs01s1' width='100%'></td>
        <td> <img src='./fig/HDemucs01WV1.PNG'  alt='hdemucs01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd01S1.PNG'  alt='hu01s1' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd01WV1.PNG'  alt='hu01wv1' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean01S1.PNG'  alt='clean01s1' width='100%'></td>
        <td> <img src='./fig/clean01WV1.PNG'  alt='clean01wv1' width='100%'></td>
    </tr>
</table>
  
<details align='right'>
  <summary>Expand binaural images</summary>
  
  <table style="margin-left: auto; margin-right: auto; align:center; border: none!important">
    <tr margin-bottom='0px'>
      <td align='center'> <b>Mixture</b> </td>
        <td> <img src='./fig/Mix01S2.PNG'  alt='mix01s2' width='100%'></td>
        <td> <img src='./fig/Mix01WV2.PNG'  alt='mix01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>ResUNetDecouple+</b> </td>
        <td> <img src='./fig/ResUNet01S2.PNG'  alt='res01s2' width='100%'></td>
        <td> <img src='./fig/ResUNet01WV2.PNG'  alt='res01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (ResUNetDecouple+)</b> </td>
        <td> <img src='./fig/preFro01S2.PNG'  alt='pre01s2' width='100%'></td>
        <td> <img src='./fig/preFro01WV2.PNG'  alt='pre01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>HDemucs</b> </td>
        <td> <img src='./fig/HDemucs01S2.PNG'  alt='hdemucs01s2' width='100%'></td>
        <td> <img src='./fig/HDemucs01WV2.PNG'  alt='hdemucs01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>VocEmb4Sep (HDemucs)</b></td>
        <td> <img src='./fig/HDemucsUpd01S2.PNG'  alt='hu01s2' width='100%'></td>
        <td> <img src='./fig/HDemucsUpd01WV2.PNG'  alt='hu01wv2' width='100%'></td>
    </tr>
    <tr>
      <td align='center'> <b>Clean</b> </td>
        <td> <img src='./fig/clean01S2.PNG'  alt='clean01s2' width='100%'></td>
        <td> <img src='./fig/clean01WV2.PNG'  alt='clean01wv2' width='100%'></td>
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
            <source src="./wav/Mix_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/ResUNet_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    	<td align='center' width='30%'>
        <audio controls>
            <source src="./wav/preFro_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    <tr>
    <td align='center'>HDemucs</td>
    <td align='center'>VocEmb4Sep (HDemucs)</td>
    <td align='center'>Clean</td>
    </tr>
    <tr>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucs_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/HDemucsUpd2_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
        <td align='center' width='30%'>
        <audio controls>
            <source src="./wav/clean_Atrophy_01.wav" type="audio/wav">
            Your browser does not support the audio element.
        </audio>
        </td>
    </tr>
    </table></div>

  
  
<!-- </html> -->

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
 -->
