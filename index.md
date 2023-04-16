## Abstract

Zero-shot voice conversion (VC) trained by non-parallel data has gained a lot of attention in recent years. Previous methods usually extract speaker embeddings from audios and use them for converting the voices into different voice styles. Since there is a strong relationship between human faces and voices, a promising approach would be to synthesize various voice characteristics from face representation. Therefore, we introduce a novel idea of generating different voice styles from different human face photos, which can facilitate new applications, e.g., personalized voice assistants.
However, the audio-visual relationship is implicit. Moreover, the existing VCs are trained on laboratory-collected datasets without speaker photos, while the datasets with both photos and audios are in-the-wild datasets. Directly replacing the target audio with the target photo and training on the in-the-wild dataset leads to noisy results. To address these issues, we propose a novel many-to-many voice conversion network, namely Face-based Voice Conversion (FaceVC), with a 3-stage training strategy. Quantitative and qualitative experiments on the LRS3-Ted dataset show that the proposed FaceVC successfully performs voice conversion according to the target face photos.

<img align="center" src="resources/arch.png" style="  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 80%;" />

## Offical Code Github REPO

https://github.com/Levent/Zeroshot-FaceVC

## Audio Samples

1. The essential point to be remembered is that the ornament, whatever it is, whether picture or pattern work, should form part of the page.

    <table style="text-align: center;">

    <tr>
    <th style="text-align: center;">Source Speaker</th>
    <th style="text-align: center;">Target Speaker</th>
    </tr>

    <tr>
    <td><img src="resources/image/mgcj_00005.jpg"></td>
    <td><img src="resources/image/7kkR_00004.jpg"></td>
    </tr>

    <tr>
    <td><audio controls="" ><source src="resources/wav/1/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_src_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/1/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.wav" type="audio/wav"></audio></td>
    </tr>

    <tr>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    </tr>
    <tbody>
    <tr>
    <td><audio controls="" ><source src="resources/wav/SpeechVC/7kkR_00003_mgcj_00008_M2F_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/wav/FVMVC/7kkR_00003_mgcj_00008_M2F_gen.wav"  type="audio/wav"></audio></td>
    </tr>
    </tbody>
    </table>


    <table style="text-align: center;">

    <tr>
    <th style="text-align: center;">Source Speaker</th>
    <th style="text-align: center;">Target Speaker</th>
    </tr>

    <tr>
    <td><img src="resources/image/mgcj_00005.jpg"></td>
    <td><img src="resources/image/7kkR_00004.jpg"></td>
    </tr>

    <tr>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.wav"></audio></td>
    </tr>

    <tr>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    </tr>
    <tbody>
    <tr>
    <td><audio controls="" ><source src="resources/wav/SpeechVC/7kkR_00003_mgcj_00008_M2F_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/wav/FVMVC/7kkR_00003_mgcj_00008_M2F_gen.wav"  type="audio/wav"></audio></td>
    </tr>
    </tbody>
    </table>


    <table style="text-align: center;">

    <tr>
    <th style="text-align: center;">Source Speaker</th>
    <th style="text-align: center;">Target Speaker</th>
    </tr>

    <tr>
    <td><img src="resources/image/mgcj_00005.jpg"></td>
    <td><img src="resources/image/7kkR_00004.jpg"></td>
    </tr>

    <tr>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.wav"></audio></td>
    </tr>

    <tr>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    </tr>
    <tbody>
    <tr>
    <td><audio controls="" ><source src="resources/wav/SpeechVC/7kkR_00003_mgcj_00008_M2F_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/wav/FVMVC/7kkR_00003_mgcj_00008_M2F_gen.wav"  type="audio/wav"></audio></td>
    </tr>
    </tbody>
    </table>



2. Consistency The essential point to be remembered is that the ornament, whatever it is, whether picture or pattern work, should form part of the page.
    <table stype='width:80%' style="text-align: center;">

    <tr>
    <th></th>
    <th style="text-align: center;">Source Speaker Wav</th>
    <th style="text-align: center;">Target Speaker Image 1</th>
    <th style="text-align: center;">Target Speaker Image 2</th>
    <th style="text-align: center;">Target Speaker Image 3</th>
    </tr>

    <tr>
    <td></td>
    <td></td>
    <td><img src="resources/img_00001.jpg"></td>
    <td><img src="resources/img_00001.jpg"></td>
    <td><img src="resources/img_00001.jpg"></td>
    </tr>

    <tr>
    <td>wav</td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT (voc.)/0000000001.mp3" type="audio/wav"></audio></td>
    </tr>


    <tr>
    <td>wav</td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT (voc.)/0000000001.mp3" type="audio/wav"></audio></td>
    </tr>


    <tr>
    <td>wav</td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT (voc.)/0000000001.mp3" type="audio/wav"></audio></td>
    </tr>

    <tr>
    <td>wav</td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/audio/GT (voc.)/0000000001.mp3" type="audio/wav"></audio></td>
    </tr>
    </table>

3. Consistency The essential point to be remembered is that the ornament, whatever it is, whether picture or pattern work, should form part of the page.
    <table stype='width:80%' style="text-align: center;">

    <tr>
    <th></th>
    <th style="text-align: center;">Speaker A</th>
    <th style="text-align: center;">Speaker B</th>
    <th></th>
    <th style="text-align: center;">Speaker C</th>
    <th style="text-align: center;">Speaker D</th>
    <th></th>
    <th style="text-align: center;">Speaker E</th>
    <th style="text-align: center;">Speaker F</th>
    </tr>

    <tr>
    <td></td>
    <td><img src="resources/img_00001.jpg"></td>
    <td><img src="resources/img_00001.jpg"></td>
    <td></td>
    <td><img src="resources/img_00001.jpg"></td>
    <td><img src="resources/img_00001.jpg"></td>
    <td></td>
    <td><img src="resources/img_00001.jpg"></td>
    <td><img src="resources/img_00001.jpg"></td>
    </tr>

    <tr>
    <td>A</td>
    <td colspan ="2" ><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td>C</td>
    <td colspan ="2" ><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td>E</td>
    <td colspan ="2" ><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    </tr>
    </table>


