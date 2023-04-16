## Abstract

Non-autoregressive text-to-speech (NAR-TTS) models such as FastSpeech 2 and Glow-TTS can synthesize high-quality speech from the given text in parallel. After analyzing two kinds of generative NAR-TTS models (VAE and normalizing flow), we find that: VAE is good at capturing the long-range semantics features (e.g., prosody) even with small model size but suffers from blurry and unnatural results; and normalizing flow is good at reconstructing the frequency bin-wise details but performs poorly when the number of model parameters is limited. Inspired by these observations, to generate diverse speech with natural details and rich prosody using a lightweight architecture, we propose PortaSpeech, a portable and high-quality generative text-to-speech model. Specifically, 1) to model both the prosody and mel-spectrogram details accurately, we adopt a lightweight VAE with an enhanced prior followed by a flow-based post-net with strong conditional inputs as the main architecture. 2) To further compress the model size and memory footprint, we introduce the grouped parameter sharing mechanism to the affine coupling layers in the post-net. 3) To improve the expressiveness of synthesized speech and reduce the dependency on accurate fine-grained alignment between text and speech, we propose a linguistic encoder with mixture alignment combining hard inter-word alignment and soft intra-word alignment, which explicitly extracts word-level semantic information.  Experimental results show that PortaSpeech outperforms other TTS models in both voice quality and prosody modeling in terms of subjective and objective evaluation metrics, and shows only a slight performance degradation when reducing the model parameters to 6.7M (about 4x model size and 3x runtime memory compression ratio compared with FastSpeech 2). Our extensive ablation studies demonstrate that each design in PortaSpeech is effective. d

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
    <th></th>
    <th style="text-align: center;">Source Speaker</th>
    <th style="text-align: center;">Target Speaker</th>
    </tr>

    <tr>
    <td><img src="resources/image/mgcj_00005.jpg"></td>
    <td><img src="resources/image/7kkR_00004.jpg"></td>
    <td></td>
    <td><img src=""></td>
    <td><img src=""></td>
    </tr>

    <tr>
    <td><audio controls="" ><source src="resources/wav/1/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_src_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/1/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.wav" type="audio/wav"></audio></td>
    <td></td>
    <td><audio controls=""><source src="resources/wav/1/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.mp3" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/1/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.mp3" type="audio/wav"></audio></td>
    </tr>

    <tr>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    <th></th>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    </tr>
    <tbody>
    <tr>
    <td><audio controls="" ><source src="resources/wav/SpeechVC/7kkR_00003_mgcj_00008_M2F_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/wav/FVMVC/7kkR_00003_mgcj_00008_M2F_gen.wav"  type="audio/wav"></audio></td>
    <td></td>
    <td><audio controls="" ><source src="resources/wav/SpeechVC/7kkR_00003_mgcj_00008_M2F_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/wav/FVMVC/7kkR_00003_mgcj_00008_M2F_gen.wav"  type="audio/wav"></audio></td>
    </tr>
    </tbody>
    </table>


    <table style="text-align: center;">

    <tr>
    <th style="text-align: center;">Source Speaker</th>
    <th style="text-align: center;">Target Speaker</th>
    <th></th>
    <th style="text-align: center;">Source Speaker</th>
    <th style="text-align: center;">Target Speaker</th>
    </tr>

    <tr>
    <td><img src="resources/image/mgcj_00005.jpg"></td>
    <td><img src="resources/image/7kkR_00004.jpg"></td>
    <td></td>
    <td><img src=""></td>
    <td><img src=""></td>
    </tr>

    <tr>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.wav"></audio></td>
    <td></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.wav"></audio></td>
    </tr>

    <tr>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    <th></th>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    </tr>
    <tbody>
    <tr>
    <td><audio controls="" ><source src="resources/wav/SpeechVC/7kkR_00003_mgcj_00008_M2F_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/wav/FVMVC/7kkR_00003_mgcj_00008_M2F_gen.wav"  type="audio/wav"></audio></td>
    <td></td>
    <td><audio controls="" ><source src="resources/wav/SpeechVC/7kkR_00003_mgcj_00008_M2F_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/wav/FVMVC/7kkR_00003_mgcj_00008_M2F_gen.wav"  type="audio/wav"></audio></td>
    </tr>
    </tbody>
    </table>


    <table style="text-align: center;">

    <tr>
    <th style="text-align: center;">Source Speaker</th>
    <th style="text-align: center;">Target Speaker</th>
    <th></th>
    <th style="text-align: center;">Source Speaker</th>
    <th style="text-align: center;">Target Speaker</th>
    </tr>

    <tr>
    <td><img src="resources/image/mgcj_00005.jpg"></td>
    <td><img src="resources/image/7kkR_00004.jpg"></td>
    <td></td>
    <td><img src=""></td>
    <td><img src=""></td>
    </tr>

    <tr>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.wav"></audio></td>
    <td></td>
    <td><audio controls="" ><source src="resources/audio/GT/0000000001.mp3" type="audio/wav"></audio></td>
    <td><audio controls=""><source src="resources/wav/ref_sour_wav/7kkR_00003_mgcj_00005_M2F_ref_gen.wav"></audio></td>
    </tr>

    <tr>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    <th></th>
    <th style="text-align: center;">SpeechVC</th>
    <th style="text-align: center;">FVMVC</th>
    </tr>
    <tbody>
    <tr>
    <td><audio controls="" ><source src="resources/wav/SpeechVC/7kkR_00003_mgcj_00008_M2F_gen.wav" type="audio/wav"></audio></td>
    <td><audio controls="" ><source src="resources/wav/FVMVC/7kkR_00003_mgcj_00008_M2F_gen.wav"  type="audio/wav"></audio></td>
    <td></td>
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


