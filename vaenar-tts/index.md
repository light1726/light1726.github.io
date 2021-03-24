# <center> VAENAR-TTS: Variational Auto-Encoder based Non-AutoRegressive Text-to-Speech Synthesis </center>

## Abstract
We describe a variational auto-encoder based non-autoregressive text-to-speech (VAENAR-TTS) model in this paper. Autoregressive TTS (AR-TTS) models based on the sequence-to-sequence architecture can generate high-quality speech. However, the sequentially decoding process of the AR-TTS models can be time-consuming. The recently proposed non-autoregressive TTS (NAR-TTS) are more efficient with parallel decoding process. However, these models rely on the phoneme-level duration to generate the hard alignment between the text and the spectrogram. The obtaining of the duration labels either through the force-alignment tool or knowledge distillation is cumbersome and the hard alignment based on phoneme expansion can hurt the naturalness of the synthesized speech. The proposed VAENAR-TTS is a more end-to-end NAR-TTS solution that does not require the phoneme-level duration labels. VAENAR-TTS consists of no recurrent structures and is completely NAR in both the training and inference phase. Based on the VAE architecture, the alignment information is encoded in the latent variable and the attention-based soft alignment between the text and the latent variable is used in the decoder to reconstruct the spectrogram. Experiments show that VAENAR-TTS achieves comparable synthesis quality with the state-of-the-art AR-TTS models while the synthesis speed is competitive to that of the NAR-TTS models.

Source Codes will be released soon!  


## Single-speaker TTS (English)

LJ007-0129. The sane and the insane, the young and the old, the trivial offender and the man about to suffer the extreme penalty of the law,

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ007-0129.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ007-0129.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ007-0129.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ007-0129.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ007-0129.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ009-0046. But the attempt fails; he trembles, his knees knock together, and his head droops as he enters the condemned pew.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ009-0046.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ012-0201. Bishop confessed that he was moved to this by the example of Burke and Hare.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ012-0201.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ012-0201.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ012-0201.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ012-0201.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ012-0201.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |


LJ015-0236. Burgess admitted him into the guard's van, where he fitted and filed the keys till they worked easily and satisfactorily in the locks of the safe.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ015-0236.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ015-0236.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ015-0236.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ015-0236.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ015-0236.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ022-0112. and I assure my fellow citizens that no energy will be spared in using these funds effectively

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ022-0112.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ022-0112.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ022-0112.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ022-0112.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ022-0112.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ033-0194. The blanket in which the rifle was stored was composed of brown and green cotton, viscose and woolen fibers.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ033-0194.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ033-0194.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ033-0194.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ033-0194.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ033-0194.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |


LJ039-0193. and a total minimum time period of from 7.1 to 7.9 seconds for all three shots.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ039-0193.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ039-0193.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ039-0193.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ039-0193.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ039-0193.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ032-0117. He lifted the rifle by the wooden stock after his examination convinced him that the wood was too rough to take fingerprints.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ032-0117.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ032-0117.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ032-0117.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ032-0117.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ032-0117.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ032-0073. purchased by mail-order coupon from Seaport-Traders, Inc., a mail-order division of George Rose and Co., Los Angeles.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ032-0073.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ032-0073.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ032-0073.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ032-0073.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ032-0073.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |

LJ047-0234. Hosty's initial reaction on hearing that Oswald was a suspect in the assassination, was, quote, shock

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ047-0234.wav" controls preload></audio> | <audio src="wavs\bvae-tts\LJ047-0234.wav" controls preload></audio> | <audio src="wavs\glow-tts\LJ047-0234.wav" controls preload></audio> | <audio src="wavs\fastspeech2\LJ047-0234.wav" controls preload></audio> | <audio src="wavs\vaenar-tts\LJ047-0234.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |


