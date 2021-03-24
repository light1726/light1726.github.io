# <center> VAENAR-TTS: Variational Auto-Encoder based Non-AutoRegressive Text-to-Speech Synthesis </center>

## Abstract
We describe a variational auto-encoder based non-autoregressive text-to-speech (VAENAR-TTS) model in this paper. Autoregressive TTS (AR-TTS) models based on the sequence-to-sequence architecture can generate high-quality speech. However, the sequentially decoding process of the AR-TTS models can be time-consuming. The recently proposed non-autoregressive TTS (NAR-TTS) are more efficient with parallel decoding process. However, these models rely on the phoneme-level duration to generate the hard alignment between the text and the spectrogram. The obtaining of the duration labels either through the force-alignment tool or knowledge distillation is cumbersome and the hard alignment based on phoneme expansion can hurt the naturalness of the synthesized speech. The proposed VAENAR-TTS is a more end-to-end NAR-TTS solution that does not require the phoneme-level duration labels. VAENAR-TTS consists of no recurrent structures and is completely NAR in both the training and inference phase. Based on the VAE architecture, the alignment information is encoded in the latent variable and the attention-based soft alignment between the text and the latent variable is used in the decoder to reconstruct the spectrogram. Experiments show that VAENAR-TTS achieves comparable synthesis quality with the state-of-the-art AR-TTS models while the synthesis speed is competitive to that of the NAR-TTS models.

Source Codes will be released soon!  


## Single-speaker TTS (English)

Text: Once held by Hobson and Dewey, now carried by Mother Eddy and Brother Dowie.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/121_121726_000025_000001.wav" controls preload></audio> | <audio src="wavs/en/bvae/121_121726_000025_000001.wav" controls preload></audio> | <audio src="wavs/en/vara/121_121726_000025_000001.wav" controls preload></audio> |
| --- | --- | --- |

Text: If the child gives the effect another turn of the screw, what do you say to TWO children?

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/121_127105_000008_000002.wav" controls preload></audio> | <audio src="wavs/en/bvae/121_127105_000008_000002.wav" controls preload></audio> | <audio src="wavs/en/vara/121_127105_000008_000002.wav" controls preload></audio> |
| --- | --- | --- |

Text: But Polly couldn't speak; and if Jasper hadn't caught her just in time, she would have tumbled over backward from the stool, Phronsie and all!

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/237_126133_000023_000000.wav" controls preload></audio> | <audio src="wavs/en/bvae/237_126133_000023_000000.wav" controls preload></audio> | <audio src="wavs/en/vara/237_126133_000023_000000.wav" controls preload></audio> |
| --- | --- | --- |


Text: "But," I remarked, "since we have followed the road that Saknussemm has shown us."

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/260_123286_000016_000000.wav" controls preload></audio> | <audio src="wavs/en/bvae/260_123286_000016_000000.wav" controls preload></audio> | <audio src="wavs/en/vara/260_123286_000016_000000.wav" controls preload></audio> |
| --- | --- | --- |

Text: Such is their ponderous weight that they cannot rise from the horizon; but, obeying an impulse from higher currents, their dense consistency slowly yields.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/260_123288_000006_000002.wav" controls preload></audio> | <audio src="wavs/en/bvae/260_123288_000006_000002.wav" controls preload></audio> | <audio src="wavs/en/vara/260_123288_000006_000002.wav" controls preload></audio> |
| --- | --- | --- |

Text: We were on the edge of the Casanova churchyard.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/533_1066_000015_000004.wav" controls preload></audio> | <audio src="wavs/en/bvae/533_1066_000015_000004.wav" controls preload></audio> | <audio src="wavs/en/vara/533_1066_000015_000004.wav" controls preload></audio> |
| --- | --- | --- |


Text: O life of this our spring! why fades the lotus of the water? Why fade these children of the spring?

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/908_157963_000010_000000.wav" controls preload></audio> | <audio src="wavs/en/bvae/908_157963_000010_000000.wav" controls preload></audio> | <audio src="wavs/en/vara/908_157963_000010_000000.wav" controls preload></audio> |
| --- | --- | --- |

Text: A ring of amethyst I could not wear here, plainer to my sight, Than that first kiss.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/908_31957_000017_000001.wav" controls preload></audio> | <audio src="wavs/en/bvae/908_31957_000017_000001.wav" controls preload></audio> | <audio src="wavs/en/vara/908_31957_000017_000001.wav" controls preload></audio> |
| --- | --- | --- |

Text: For a full hour he had paced up and down, waiting: but he could wait no longer.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/1089_134691_000002_000002.wav" controls preload></audio> | <audio src="wavs/en/bvae/1089_134691_000002_000002.wav" controls preload></audio> | <audio src="wavs/en/vara/1089_134691_000002_000002.wav" controls preload></audio> |
| --- | --- | --- |

Text: For a long time he had wished to explore the beautiful Land of Oz in which they lived.

| **Tacotron 2** | **BVAE-TTS** | **Glow-TTS** | **FastSpeech2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- |
| <audio src="wavs/en/taco2/1284_1180_000006_000002.wav" controls preload></audio> | <audio src="wavs/en/bvae/1284_1180_000006_000002.wav" controls preload></audio> | <audio src="wavs/en/vara/1284_1180_000006_000002.wav" controls preload></audio> |
| --- | --- | --- |


