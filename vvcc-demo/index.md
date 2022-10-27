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
| 1 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p225_166-to-p234.wav" controls preload></audio> | <audio src="wavs/targets/vc-p225_166-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p225_166-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p225_166-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p225_166-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p225_166-to-p234.wav" controls preload></audio> |
| 2 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p225_363-to-p335.wav" controls preload></audio> | <audio src="wavs/targets/vc-p225_363-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p225_363-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p225_363-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p225_363-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p225_363-to-p335.wav" controls preload></audio> |
| 3 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p234_045-to-p302.wav" controls preload></audio> | <audio src="wavs/targets/vc-p234_045-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p234_045-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p234_045-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p234_045-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p234_045-to-p302.wav" controls preload></audio> |
| 4 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p234_115-to-p347.wav" controls preload></audio> | <audio src="wavs/targets/vc-p234_115-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p234_115-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p234_115-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p234_115-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p234_115-to-p347.wav" controls preload></audio> |
| 5 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p238_021-to-p335.wav" controls preload></audio> | <audio src="wavs/targets/vc-p238_021-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p238_021-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p238_021-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p238_021-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p238_021-to-p335.wav" controls preload></audio> |
| 6 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p238_129-to-p234.wav" controls preload></audio> | <audio src="wavs/targets/vc-p238_129-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p238_129-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p238_129-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p238_129-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p238_129-to-p234.wav" controls preload></audio> |
| 7 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p245_101-to-p238.wav" controls preload></audio> | <audio src="wavs/targets/vc-p245_101-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p245_101-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p245_101-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p245_101-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p245_101-to-p238.wav" controls preload></audio> |
| 8 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p245_117-to-p225.wav" controls preload></audio> | <audio src="wavs/targets/vc-p245_117-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p245_117-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p245_117-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p245_117-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p245_117-to-p225.wav" controls preload></audio> |
| 9 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p248_348-to-p347.wav" controls preload></audio> | <audio src="wavs/targets/vc-p248_348-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p248_348-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p248_348-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p248_348-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p248_348-to-p347.wav" controls preload></audio> |
| 10 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p261_265-to-p225.wav" controls preload></audio> | <audio src="wavs/targets/vc-p261_265-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p261_265-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p261_265-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p261_265-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p261_265-to-p225.wav" controls preload></audio> |
| 11 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p294_176-to-p326.wav" controls preload></audio> | <audio src="wavs/targets/vc-p294_176-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p294_176-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p294_176-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p294_176-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p294_176-to-p326.wav" controls preload></audio> |
| 12 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p302_276-to-p294.wav" controls preload></audio> | <audio src="wavs/targets/vc-p302_276-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p302_276-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p302_276-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p302_276-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p302_276-to-p294.wav" controls preload></audio> |
| 13 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p326_370-to-p245.wav" controls preload></audio> | <audio src="wavs/targets/vc-p326_370-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p326_370-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p326_370-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p326_370-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p326_370-to-p245.wav" controls preload></audio> |
| 14 |<audio src="wavs/voice_conversion/0.hifi-gan-src/vc-p347_336-to-p261.wav" controls preload></audio> | <audio src="wavs/targets/vc-p347_336-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_conversion/1.vqmivc/vc-p347_336-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_conversion/2.sc-glowtts/vc-p347_336-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_conversion/3.vvc/vc-p347_336-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_conversion/4.vvcc/vc-p347_336-to-p261.wav" controls preload></audio> |
| --- | --- | --- | --- | --- | --- | --- |

<h2>3. Voice Cloning Samples<a name="vcl-comp"></a></h2>

1. He knew now that his absence, for as long as he had to be away, would be covered up and satisfactorily accounted for.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-37-to-p248.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-37-to-p248.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-37-to-p248.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-37-to-p248.wav" controls preload></audio> |
| --- | --- | --- | --- |

2. After all, the Mormon people regard the advent of the Buchanan army as one of the greatest material blessings ever brought to them.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-45-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-45-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-45-to-p335.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-45-to-p335.wav" controls preload></audio> |
| --- | --- | --- | --- |

3. Rodolfo meanwhile having returned home, and having missed the crucifix, guessed who had taken it, but gave himself no concern about it.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-6-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-6-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-6-to-p234.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-6-to-p234.wav" controls preload></audio> |
| --- | --- | --- | --- |

4. While we were planning the raid it was intended that I should be one of the party to go into the bank.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-44-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-44-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-44-to-p294.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-44-to-p294.wav" controls preload></audio> |
| --- | --- | --- | --- |

5. With thee have I wandered about in the remotest, coldest worlds, like a phantom that voluntarily haunteth winter roofs and snows.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-13-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-13-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-13-to-p261.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-13-to-p261.wav" controls preload></audio> |
| --- | --- | --- | --- |

6. Nay, I rather thrilled, Distrusting every light that seemed to gild The onward path, and feared to overlean A finger even.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-36-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-36-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-36-to-p245.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-36-to-p245.wav" controls preload></audio> |
| --- | --- | --- | --- |

7. My new friend was a poet as I was; he was an admirer of Italian literature, while I admired the French.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-8-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-8-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-8-to-p302.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-8-to-p302.wav" controls preload></audio> |
| --- | --- | --- | --- |

8. O life of this our spring! why fades the lotus of the water? Why fade these children of the spring?

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-29-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-29-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-29-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-29-to-p238.wav" controls preload></audio> |
| --- | --- | --- | --- |

9. Very much of squalor and discomfort will be endured before the last trinket or the last pretense of pecuniary decency is put away.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-4-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-4-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-4-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-4-to-p347.wav" controls preload></audio> |
| --- | --- | --- | --- |

10. Thus far the universal animal was made in the divine image, but the other animals were not as yet included in him.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-49-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-49-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-49-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-49-to-p225.wav" controls preload></audio> |
| --- | --- | --- | --- |

11. Well, said Franz with a sigh, do as you please my dear viscount, for your arguments are beyond my powers of refutation.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-21-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-21-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-21-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-21-to-p326.wav" controls preload></audio> |
| --- | --- | --- | --- |

12. Forthwith the grinning Jester began shrieking with laughter, so that the bells upon his motley cap were all set a jangling.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-18-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-18-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-18-to-p326.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-18-to-p326.wav" controls preload></audio> |
| --- | --- | --- | --- |

13. However loudly outward circumstances might oppose this, he now felt, with a certainty which surprised him, that this work was not his own.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-10-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-10-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-10-to-p225.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-10-to-p225.wav" controls preload></audio> |
| --- | --- | --- | --- |

14. I will briefly describe them to you, and you shall read the account of them at your leisure in the sacred registers.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-22-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-22-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-22-to-p347.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-22-to-p347.wav" controls preload></audio> |
| --- | --- | --- | --- |

15. One perceives, without understanding it, a hideous murmur, sounding almost like human accents, but more nearly resembling a howl than an articulate word.

| **Reference** |**SC-GlowTTS**| **CDFSE** | **VVCC(ours)**|
| :--- | :--- | :--- | :--- |
| <audio src="wavs/voice_cloning/6.hifi-gan-tgt/tts-31-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/2.sc-glowtts/tts-31-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/5.cdfse/tts-31-to-p238.wav" controls preload></audio> | <audio src="wavs/voice_cloning/4.vvcc/tts-31-to-p238.wav" controls preload></audio> |
| --- | --- | --- | --- |
