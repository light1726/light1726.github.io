<h2><center> A Unified Framework for One-Shot Voice Conversion and Cloning Using Variational Auto-Encoder </center></h2>

<h2>0. Contents</h2>
1. [Abstract](#abstract)
2. [Comparison models and their implementations](#implementations)
3. [Voice Conversion Samples](#vc-comp)
4. [Voice Cloning Samples](#vcl-comp)

<h2>1. Abstract<a name="abstract"></a></h2>

We propose to unify one-shot voice conversion and cloning in a single model that can be optimized end-to-end. We adopt a variational auto-encoder (VAE) to disentangle speech into the content and speaker representations. Instead of imposing a fixed Gaussian prior for the content representation learning, we incorporate a novel learnable text-aware prior as an informative guide. In this way, the content representation can be better learned with less entangled speaker information and more linguistic information encoded. Since the content representation can be either sampled from the speech-conditioned posterior or the text-aware prior, voice conversion and cloning can be respectively achieved by combining the content representation with the speaker representation. We evaluate the proposed method for both one-shot voice conversion and cloning. Both the objective and subjective evaluations show the effectiveness of the proposed framework. 


<h2>2. Comparison models and their implementations<a name="implementations"></a></h2>

<h3>Below lists the implementations we used in our experiments. We adopt the same test set.</h3>

[SC-GlowTTS: Google Colab](https://colab.research.google.com/drive/1yyQDc-xWCqa2g-d1joW_goqbYZKaImsJ?usp=sharing)

[CDFSE: https://github.com/thuhcsi/interspeech2022-cdfse-tts](https://github.com/thuhcsi/interspeech2022-cdfse-tts)

[VQMIVC: https://github.com/Wendison/VQMIVC](https://github.com/Wendison/VQMIVC)

<h3>The below official Hifi-GAN pre-trained model is used.</h3>

[Hifi-GAN (official): VCTK-V1](https://drive.google.com/drive/folders/1vJlfkwR7Uyheq2U5HrPnfTm-tzwuNuey)

<h2>3. Voice Conversion Samples<a name="vc-comp"></a></h2>

| ID | **Source** | **Reference** | **VQMIVC**  |**SC-GlowTTS**| **VVC** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p225_017-to-p238.wav" controls preload></audio> | <audio src="wavs/targets/vc-p225_017-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p225_017-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p225_017-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p225_017-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p225_017-to-p238.wav" controls preload></audio> |
| 2 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p225_258-to-p302.wav" controls preload></audio> | <audio src="wavs/targets/vc-p225_258-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p225_258-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p225_258-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p225_258-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p225_258-to-p302.wav" controls preload></audio> |
| 3 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p234_109-to-p245.wav" controls preload></audio> | <audio src="wavs/targets/vc-p234_109-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p234_109-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p234_109-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p234_109-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p234_109-to-p245.wav" controls preload></audio> |
| 4 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p234_115-to-p294.wav" controls preload></audio> | <audio src="wavs/targets/vc-p234_115-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p234_115-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p234_115-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p234_115-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p234_115-to-p294.wav" controls preload></audio> |
| 5 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p238_021-to-p347.wav" controls preload></audio> | <audio src="wavs/targets/vc-p238_021-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p238_021-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p238_021-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p238_021-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p238_021-to-p347.wav" controls preload></audio> |
| 6 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p238_114-to-p225.wav" controls preload></audio> | <audio src="wavs/targets/vc-p238_114-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p238_114-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p238_114-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p238_114-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p238_114-to-p225.wav" controls preload></audio> |
| 7 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p302_029-to-p234.wav" controls preload></audio> | <audio src="wavs/targets/vc-p302_029-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p302_029-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p302_029-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p302_029-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p302_029-to-p234.wav" controls preload></audio> |
| 8 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p302_034-to-p326.wav" controls preload></audio> | <audio src="wavs/targets/vc-p302_034-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p302_034-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p302_034-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p302_034-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p302_034-to-p326.wav" controls preload></audio> |
| 9 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p326_350-to-p261.wav" controls preload></audio> | <audio src="wavs/targets/vc-p326_350-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p326_350-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p326_350-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p326_350-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p326_350-to-p261.wav" controls preload></audio> |
| 10 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p326_350-to-p347.wav" controls preload></audio> | <audio src="wavs/targets/vc-p326_350-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p326_350-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p326_350-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p326_350-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p326_350-to-p347.wav" controls preload></audio> |
| 11 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p347_336-to-p238.wav" controls preload></audio> | <audio src="wavs/targets/vc-p347_336-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p347_336-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p347_336-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p347_336-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p347_336-to-p238.wav" controls preload></audio> |
| 12 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p347_405-to-p238.wav" controls preload></audio> | <audio src="wavs/targets/vc-p347_405-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p347_405-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p347_405-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p347_405-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p347_405-to-p238.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- | --- |

<h2>3. Voice Cloning Samples<a name="vcl-comp"></a></h2>

1. Its creed provides for the protection of all men in their rights of worship according to the dictates of conscience.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-9-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-9-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-9-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-9-to-p225.wav" controls preload></audio> |
| --- | --- | --- | --- |

2. He thought he detected a pleasant smell of herbs, like the potpourri his mother had in bowls in their house.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-1-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-1-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-1-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-1-to-p234.wav" controls preload></audio> |
| --- | --- | --- | --- |

3. Poor Rachel! her nature recoiled from deceit, and she told, at all events, as much of the truth as she dared.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-30-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-30-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-30-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-30-to-p238.wav" controls preload></audio> |
| --- | --- | --- | --- |

4. She lay awake very long this night, planning how to lessen the evil influence of their Milton life on her mother.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-28-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-28-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-28-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-28-to-p245.wav" controls preload></audio> |
| --- | --- | --- | --- |

5. When we came up I told Miller to shut the bank door, which they had left open in their hurry.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-2-to-p248.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-2-to-p248.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-2-to-p248.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-2-to-p248.wav" controls preload></audio> |
| --- | --- | --- | --- |

6. Rodolfo meanwhile having returned home, and having missed the crucifix, guessed who had taken it, but gave himself no concern about it.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-6-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-6-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-6-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-6-to-p261.wav" controls preload></audio> |
| --- | --- | --- | --- |

7. Only, even though love has wholly disappeared, she still claims consideration, and Althea did not wish to lose Hermon's regard.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-47-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-47-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-47-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-47-to-p294.wav" controls preload></audio> |
| --- | --- | --- | --- |

8. Very much of squalor and discomfort will be endured before the last trinket or the last pretense of pecuniary decency is put away.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-4-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-4-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-4-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-4-to-p302.wav" controls preload></audio> |
| --- | --- | --- | --- |

9. So the Castrato began to speak him fair and say to him, O my lord, take this purse and go with me.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-14-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-14-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-14-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-14-to-p326.wav" controls preload></audio> |
| --- | --- | --- | --- |

10. The marquis of Worcester, a man past eighty four, was the last in England that submitted to the authority of the parliament.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-20-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-20-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-20-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-20-to-p335.wav" controls preload></audio> |
| --- | --- | --- | --- |

11. I will briefly describe them to you, and you shall read the account of them at your leisure in the sacred registers.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-22-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-22-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-22-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-22-to-p347.wav" controls preload></audio> |
| --- | --- | --- | --- |
