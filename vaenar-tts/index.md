# <center> VAENAR-TTS: Variational Auto-Encoder based Non-AutoRegressive Text-to-Speech Synthesis </center>

## Abstract
We describe a variational auto-encoder based non-autoregressive text-to-speech (VAENAR-TTS) model in this paper. Autoregressive TTS (AR-TTS) models based on the sequence-to-sequence architecture can generate high-quality speech. However, the sequentially decoding process of the AR-TTS models can be time-consuming. The recently proposed non-autoregressive TTS (NAR-TTS) are more efficient with parallel decoding process. However, these models rely on the phoneme-level duration to generate the hard alignment between the text and the spectrogram. The obtaining of the duration labels either through the force-alignment tool or knowledge distillation is cumbersome and the hard alignment based on phoneme expansion can hurt the naturalness of the synthesized speech. The proposed VAENAR-TTS is a more end-to-end NAR-TTS solution that does not require the phoneme-level duration labels. VAENAR-TTS consists of no recurrent structures and is completely NAR in both the training and inference phase. Based on the VAE architecture, the alignment information is encoded in the latent variable and the attention-based soft alignment between the text and the latent variable is used in the decoder to reconstruct the spectrogram. Experiments show that VAENAR-TTS achieves comparable synthesis quality with the state-of-the-art AR-TTS models while the synthesis speed is competitive to that of the NAR-TTS models.

Source Codes will be released soon!  

## Implementations of the compared models

[Tacotron2](https://github.com/NVIDIA/tacotron2)
[FastSpeech2](https://github.com/ming024/FastSpeech2)
[BVAE-TTS (official)](https://github.com/LEEYOONHYUNG/BVAE-TTS)
[Glow-TTS (official)](https://github.com/jaywalnut310/glow-tts)

## Single-speaker TTS (English)

LJ003-0305. The provision of more baths was also suggested, and the daily sweeping out of the prison.

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ003-0305.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ009-0046. But the attempt fails; he trembles, his knees knock together, and his head droops as he enters the condemned pew.

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ009-0046.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ005-0100. For this purpose it kept up an extensive correspondence with all parts of the kingdom, and circulated queries to be answered in detail,

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ005-0100.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ005-0100.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ005-0100.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ005-0100.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ005-0100.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |


LJ006-0206. and publications which in these days would have been made the subject of a criminal prosecution.

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ006-0206.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ006-0206.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ006-0206.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ006-0206.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ006-0206.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ007-0177. We trust, however, that the day is at hand when this stain will be removed from the character of the city of London,

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ007-0177.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ007-0177.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ007-0177.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ007-0177.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ007-0177.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ013-0081. Banks and bankers continued to be victimized.

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ013-0081.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ013-0081.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ013-0081.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ013-0081.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ013-0081.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |


LJ038-0009. When he heard police sirens, he, quote, looked up and saw the man enter the lobby, end quote.

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ038-0009.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ038-0009.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ038-0009.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ038-0009.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ038-0009.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ041-0099. Powers believed that when Oswald arrived in Japan he acquired a girlfriend, quote,

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ041-0099.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ041-0099.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ041-0099.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ041-0099.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ041-0099.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ043-0071. His performance for that company was satisfactory.

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ043-0071.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ043-0071.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ043-0071.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ043-0071.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ043-0071.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ047-0234. Hosty's initial reaction on hearing that Oswald was a suspect in the assassination, was, quote, shock

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ047-0234.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ047-0234.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ047-0234.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ047-0234.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ047-0234.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

## Attention Alignemnt convergence speed of models with different reduction factor
### Reduction factor = 3
![Reduction factor = 3](./images/R3.gif)
### Reduction factor = 4
![Reduction factor = 4](./images/R4.gif)
### Reduction factor = 5
![Reduction factor = 5](./images/R5.gif)
