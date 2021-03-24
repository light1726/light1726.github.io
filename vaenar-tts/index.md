# <center> VAENAR-TTS: Variational Auto-Encoder based Non-AutoRegressive Text-to-Speech Synthesis </center>

## Abstract
We describe a variational auto-encoder based non-autoregressive text-to-speech (VAENAR-TTS) model in this paper. Autoregressive TTS (AR-TTS) models based on the sequence-to-sequence architecture can generate high-quality speech. However, the sequentially decoding process of the AR-TTS models can be time-consuming. The recently proposed non-autoregressive TTS (NAR-TTS) are more efficient with parallel decoding process. However, these models rely on the phoneme-level duration to generate the hard alignment between the text and the spectrogram. The obtaining of the duration labels either through the force-alignment tool or knowledge distillation is cumbersome and the hard alignment based on phoneme expansion can hurt the naturalness of the synthesized speech. The proposed VAENAR-TTS is a more end-to-end NAR-TTS solution that does not require the phoneme-level duration labels. VAENAR-TTS consists of no recurrent structures and is completely NAR in both the training and inference phase. Based on the VAE architecture, the alignment information is encoded in the latent variable and the attention-based soft alignment between the text and the latent variable is used in the decoder to reconstruct the spectrogram. Experiments show that VAENAR-TTS achieves comparable synthesis quality with the state-of-the-art AR-TTS models while the synthesis speed is competitive to that of the NAR-TTS models.

Source Codes will be released soon!  


## Single-speaker TTS (English)

LJ007-0129. The sane and the insane, the young and the old, the trivial offender and the man about to suffer the extreme penalty of the law,

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs\tacotron2\LJ007-0129.wav" controls preload></audio> | <audio src="wavs/en/bvae/121_121726_000025_000001.wav" controls preload></audio> | <audio src="wavs/en/vara/121_121726_000025_000001.wav" controls preload></audio> |
| --- | --- | --- |

LJ009-0046. But the attempt fails; he trembles, his knees knock together, and his head droops as he enters the condemned pew.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/121_127105_000008_000002.wav" controls preload></audio> | <audio src="wavs/en/bvae/121_127105_000008_000002.wav" controls preload></audio> | <audio src="wavs/en/vara/121_127105_000008_000002.wav" controls preload></audio> |
| --- | --- | --- |

LJ012-0201. Bishop confessed that he was moved to this by the example of Burke and Hare.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/237_126133_000023_000000.wav" controls preload></audio> | <audio src="wavs/en/bvae/237_126133_000023_000000.wav" controls preload></audio> | <audio src="wavs/en/vara/237_126133_000023_000000.wav" controls preload></audio> |
| --- | --- | --- |


LJ015-0236. Burgess admitted him into the guard's van, where he fitted and filed the keys till they worked easily and satisfactorily in the locks of the safe.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/260_123286_000016_000000.wav" controls preload></audio> | <audio src="wavs/en/bvae/260_123286_000016_000000.wav" controls preload></audio> | <audio src="wavs/en/vara/260_123286_000016_000000.wav" controls preload></audio> |
| --- | --- | --- |

LJ022-0112. and I assure my fellow citizens that no energy will be spared in using these funds effectively

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/260_123288_000006_000002.wav" controls preload></audio> | <audio src="wavs/en/bvae/260_123288_000006_000002.wav" controls preload></audio> | <audio src="wavs/en/vara/260_123288_000006_000002.wav" controls preload></audio> |
| --- | --- | --- |

LJ033-0194. The blanket in which the rifle was stored was composed of brown and green cotton, viscose and woolen fibers.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/533_1066_000015_000004.wav" controls preload></audio> | <audio src="wavs/en/bvae/533_1066_000015_000004.wav" controls preload></audio> | <audio src="wavs/en/vara/533_1066_000015_000004.wav" controls preload></audio> |
| --- | --- | --- |


LJ039-0193. and a total minimum time period of from 7.1 to 7.9 seconds for all three shots.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/908_157963_000010_000000.wav" controls preload></audio> | <audio src="wavs/en/bvae/908_157963_000010_000000.wav" controls preload></audio> | <audio src="wavs/en/vara/908_157963_000010_000000.wav" controls preload></audio> |
| --- | --- | --- |

LJ032-0117. He lifted the rifle by the wooden stock after his examination convinced him that the wood was too rough to take fingerprints.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/908_31957_000017_000001.wav" controls preload></audio> | <audio src="wavs/en/bvae/908_31957_000017_000001.wav" controls preload></audio> | <audio src="wavs/en/vara/908_31957_000017_000001.wav" controls preload></audio> |
| --- | --- | --- |

LJ027-0173. The caducibranch takes first the fish form, then the perennibranch form, and finally the caducibranch form, but goes no further.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/1089_134691_000002_000002.wav" controls preload></audio> | <audio src="wavs/en/bvae/1089_134691_000002_000002.wav" controls preload></audio> | <audio src="wavs/en/vara/1089_134691_000002_000002.wav" controls preload></audio> |
| --- | --- | --- |

LJ047-0234. Hosty's initial reaction on hearing that Oswald was a suspect in the assassination, was, quote, shock

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/1284_1180_000006_000002.wav" controls preload></audio> | <audio src="wavs/en/bvae/1284_1180_000006_000002.wav" controls preload></audio> | <audio src="wavs/en/vara/1284_1180_000006_000002.wav" controls preload></audio> |
| --- | --- | --- |


