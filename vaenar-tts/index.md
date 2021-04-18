# <center> VAENAR-TTS: Variational Auto-Encoder based Non-AutoRegressive Text-to-Speech Synthesis </center>

<h2>0. Contents</h2>
1. [Abstract](#abstract)
2. [Comparison models and their implementations](#implementations)
3. [Synthesized samples -- Comparison with other models](#samples-comp)
4. [Synthesized samples -- Fixed reduction factors](#samples-rf)
5. [synthesized samples -- W/ V.S. W/O causality mask](#samples-mask)
6. [Attention alignemnt convergence dynamics](#alignments)
7. [Other results](#others)

<h2>1. Abstract<a name="abstract"></a></h2>

This paper describes a variational auto-encoder based non-autoregressive text-to-speech (VAENAR-TTS) model. The autoregressive TTS (AR-TTS) models based on the sequence-to-sequence architecture can generate high-quality speech, but their sequential decoding process can be time-consuming. Recently, non-autoregressive TTS (NAR-TTS) models have been shown to be more efficient with the parallel decoding process. However, these NAR-TTS models rely on phoneme-level durations to generate a hard alignment between the text and the spectrogram. Obtaining duration labels, either through force-alignment or knowledge distillation, is cumbersome. Furthermore, hard alignment based on phoneme expansion can degrade the naturalness of the synthesized speech. In contrast, the proposed model of VAENAR-TTS is an end-to-end approach that does not require phoneme-level duration. VAENAR-TTS model does not contain recurrent structures and is completely non-autoregressive in both the training and inference phase. Based on the VAE architecture, the alignment information is encoded in the latent variable, and the attention-based soft alignment between the text and the latent variable is used in the decoder to reconstruct the spectrogram. Experiments show that VAENAR-TTS achieves state-of-the-art synthesis quality, while the synthesis speed is comparable with other NAR-TTS models.

Source Codes will be released soon!  


<h2>2. Comparison models and their implementations<a name="implementations"></a></h2>

<h3>Below lists the implementations we used in our experiments. These models are trained and evaluated with our own dataset separation configuration, while all other settings are the default.</h3>

[Tacotron2: https://github.com/NVIDIA/tacotron2](https://github.com/NVIDIA/tacotron2)

[FastSpeech2: https://github.com/ming024/FastSpeech2](https://github.com/ming024/FastSpeech2)

[BVAE-TTS (official): https://github.com/LEEYOONHYUNG/BVAE-TTS](https://github.com/LEEYOONHYUNG/BVAE-TTS)

[Glow-TTS (official): https://github.com/jaywalnut310/glow-tts](https://github.com/jaywalnut310/glow-tts)

<h3>The below official Hifi-GAN implementation is used.</h3>

[Hifi-GAN (official): https://github.com/jik876/hifi-gan]( https://github.com/jik876/hifi-gan)

<h2>3. Synthesized samples -- Comparison with other models<a name="samples-comp"></a></h2>

<h3>Below lists the samples that are synthesized for the subjective evaluation.</h3>

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

<h2>4. Synthesized samples -- Different reduction factors<a name="samples-rf"></a></h2>

<h3>Below lists samples synthesized by models with different fixed reduction factors. The evaluation results show that RF3 and RF4 are comparable and both is much better than RF5 in terms of speech naturalness</h3>

LJ003-0305. The provision of more baths was also suggested, and the daily sweeping out of the prison.

| **RF5** | **RF4** | **RF3** |
| :--- | :--- | :--- |
| <audio src="wavs\7.VAENAR-TTS-R-5\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\8.VAENAR-TTS-R-4\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\9.VAENAR-TTS-R-3\LJ003-0305.wav" controls preload></audio> |
| --- | --- | --- |

LJ009-0046. But the attempt fails; he trembles, his knees knock together, and his head droops as he enters the condemned pew.

| **RF5** | **RF4** | **RF3** |
| :--- | :--- | :--- |
| <audio src="wavs\7.VAENAR-TTS-R-5\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\8.VAENAR-TTS-R-4\LJ009-0046.wav" controls preload></audio> | <audio src="wavs\9.VAENAR-TTS-R-3\LJ009-0046.wav" controls preload></audio> |
| --- | --- | --- |

LJ005-0100. For this purpose it kept up an extensive correspondence with all parts of the kingdom, and circulated queries to be answered in detail,

| **RF5** | **RF4** | **RF3** |
| :--- | :--- | :--- |
| <audio src="wavs\7.VAENAR-TTS-R-5\LJ005-0100.wav" controls preload></audio> | <audio src="wavs\8.VAENAR-TTS-R-4\LJ005-0100.wav" controls preload></audio> | <audio src="wavs\9.VAENAR-TTS-R-3\LJ005-0100.wav" controls preload></audio> |
| --- | --- | --- |


LJ006-0206. and publications which in these days would have been made the subject of a criminal prosecution.

| **RF5** | **RF4** | **RF3** |
| :--- | :--- | :--- |
| <audio src="wavs\7.VAENAR-TTS-R-5\LJ006-0206.wav" controls preload></audio> | <audio src="wavs\8.VAENAR-TTS-R-4\LJ006-0206.wav" controls preload></audio> | <audio src="wavs\9.VAENAR-TTS-R-3\LJ006-0206.wav" controls preload></audio> |
| --- | --- | --- |

LJ007-0177. We trust, however, that the day is at hand when this stain will be removed from the character of the city of London,

| **RF5** | **RF4** | **RF3** |
| :--- | :--- | :--- |
| <audio src="wavs\7.VAENAR-TTS-R-5\LJ007-0177.wav" controls preload></audio> | <audio src="wavs\8.VAENAR-TTS-R-4\LJ007-0177.wav" controls preload></audio> | <audio src="wavs\9.VAENAR-TTS-R-3\LJ007-0177.wav" controls preload></audio> |
| --- | --- | --- |

<h2>5. synthesized samples -- W/ V.S. W/O causality mask<a name="samples-mask"></a></h2>

<h3>Below lists the samples synthesized by VAENAR-TTS with and without causality mask in the self-attention structures that are stacked on the frame-level features. The repetition issues is very common in model w/o causality mask. Pay attention to the word(s) highlighted in red color.</h3>

LJ001-0133. One very important matter in "setting up" for fine printing <span style="color:red">is</span> the "spacing," that is, the lateral distance of words from one another.

| **W/ Causality Mask** | **W/O Causality Mask** |
| :--- | :--- |
| <audio src="wavs\VAENAR-TTS-mask\LJ001-0133.wav" controls preload></audio> | <audio src="wavs\VAENAR-TTS-nomask\LJ001-0133.wav" controls preload></audio> |
| --- | --- |

LJ003-0238. and they were exacted to relieve a rich corporation from <span style="color:red">paying</span> for the maintenance of their own prison.

| **W/ Causality Mask** | **W/O Causality Mask** |
| :--- | :--- |
| <audio src="wavs\VAENAR-TTS-mask\LJ003-0238.wav" controls preload></audio> | <audio src="wavs\VAENAR-TTS-nomask\LJ003-0238.wav" controls preload></audio> |
| --- | --- |

LJ006-0006. I shall now return to the great jail of the city of London, and give a more <span style="color:red">detailed</span> account of its condition and inner life

| **W/ Causality Mask** | **W/O Causality Mask*** |
| :--- | :--- |
| <audio src="wavs\VAENAR-TTS-mask\LJ006-0006.wav" controls preload></audio> | <audio src="wavs\VAENAR-TTS-nomask\LJ006-0006.wav" controls preload></audio> |
| --- | --- |

LJ009-0208. erected on the cart, about four feet high at the head, and <span style="color:red">gradually</span> sloping towards the horse, giving a full <span style="color:red">view</span> of the body,

| **W/ Causality Mask** | **W/O Causality Mask** |
| :--- | :--- |
| <audio src="wavs\VAENAR-TTS-mask\LJ009-0208.wav" controls preload></audio> | <audio src="wavs\VAENAR-TTS-nomask\LJ009-0208.wav" controls preload></audio> |
| --- | --- |

LJ014-0054. a maidservant, Sarah Thomas, murdered her mistress, an <span style="color:red">aged</span> woman, by beating <span style="color:red">out her</span> brains with a stone.

| **W/ Causality Mask** | **W/O Causality Mask** |
| :--- | :--- |
| <audio src="wavs\VAENAR-TTS-mask\LJ014-0054.wav" controls preload></audio> | <audio src="wavs\VAENAR-TTS-nomask\LJ014-0054.wav" controls preload></audio> |
| --- | --- |

<h2>6. Attention Alignemnt convergence dynamics<a name="alignments"></a></h2>

<h3>Below are the attention alignment maps obtained during the training process of three models with different fixed reduction factors: 5, 4, and 3. Note that the alignment converges faster for the model with a larger reduction factor.</h3>

### Reduction factor = 3
![Reduction factor = 3](./images/R3.gif)

### Reduction factor = 4
![Reduction factor = 4](./images/R4.gif)

### Reduction factor = 5
![Reduction factor = 5](./images/R5.gif)

<h2>7. Other results <a name="others"></a></h2>

<h3>Synthesized results in Madarin</h3>

Trained on dataset [DataBaker](https://www.data-baker.com/open_source.html).

003095.失恋的人特别喜欢往人烟罕至的角落里钻。

<audio src="wavs\VAENAR-databaker\prior-003095-2000.wav" controls preload></audio>

003684.天安门广场，一派春意盎然。

<audio src="wavs\VAENAR-databaker\prior-003684-2000.wav" controls preload></audio>

004539.网友“甄巍峰”说，希望规范用工制度和用工秩序。

<audio src="wavs\VAENAR-databaker\prior-004539-2000.wav" controls preload></audio>

005134.我的性格也是逆来顺受，从小胆小怕事，凡事都忍让。

<audio src="wavs\VAENAR-databaker\prior-005134-2000.wav" controls preload></audio>

007732.乘客对车上负责讲解的导乘员普遍表示满意。

<audio src="wavs\VAENAR-databaker\prior-007732-2000.wav" controls preload></audio>
