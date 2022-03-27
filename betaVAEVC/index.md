# <center> Disentangled Speech Representation Learning for One-Shot Voice Conversion and Cloning </center>

<h2>0. Contents</h2>
1. [Abstract](#abstract)
2. [Samples](#samples-comp)

<h2>1. Abstract<a name="abstract"></a></h2>

Learning disentangled speaker and content representations is a fundamental question for speech representation learning.Existing methods typically apply auto-encoder to do the disentanglement while the key is to eliminate the speaker information from the content representation. Our solution is to apply the recent proposed $\beta$-VAE and use the weight $\beta$ for the Kullback-Leibler divergence to restrict the information captured by the content representation. In addition to the evidence lower bound objective, a discriminative objective to regularize the speaker representation has also been imposed. We show quantitatively that with a proper $\beta$, the speaker identity can be largely eliminated from the content representation, with the linguistic information being mostly retained. Qualitative evaluations show that one-shot voice conversion, which is a direct application of the disentangled representation learning, can be achieved with satisfying performance. In addition, we show that texts can be further utilized to regularize the content representation to make it more speaker-invariant and content-related. We do this by introducing a text conditioned prior for content representation, which enables high-quality one-shot voice cloning as a side-product. 


<h2>3. Samples <a name="samples-comp"></a></h2>

p270_012_to_p293_158. Throughout the centuries people have explained the rainbow in various ways.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p270_012_to_p293_158.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p270_012_to_p293_158.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p270_012_to_p293_158.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p270_012_to_p293_158.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p270_012_to_p293_158.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p270_012_to_p293_158.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p270_012_to_p314_007. Throughout the centuries people have explained the rainbow in various ways.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p270_012_to_p314_007.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p270_012_to_p314_007.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p270_012_to_p314_007.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p270_012_to_p314_007.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p270_012_to_p314_007.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p270_012_to_p314_007.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p270_012_to_p374_357. Throughout the centuries people have explained the rainbow in various ways.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p270_012_to_p374_357.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p270_012_to_p374_357.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p270_012_to_p374_357.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p270_012_to_p374_357.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p270_012_to_p374_357.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p270_012_to_p374_357.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p270_244_to_p293_158. Corporate banking would be based in Edinburgh.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p270_244_to_p293_158.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p270_244_to_p293_158.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p270_244_to_p293_158.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p270_244_to_p293_158.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p270_244_to_p293_158.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p270_244_to_p293_158.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p270_244_to_p314_007. Corporate banking would be based in Edinburgh.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p270_244_to_p314_007.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p270_244_to_p314_007.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p270_244_to_p314_007.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p270_244_to_p314_007.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p270_244_to_p314_007.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p270_244_to_p314_007.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p270_244_to_p374_357. Corporate banking would be based in Edinburgh.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p270_244_to_p374_357.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p270_244_to_p374_357.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p270_244_to_p374_357.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p270_244_to_p374_357.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p270_244_to_p374_357.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p270_244_to_p374_357.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p293_010_to_p270_095. People look, but no one ever finds it.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p293_010_to_p270_095.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p293_010_to_p270_095.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p293_010_to_p270_095.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p293_010_to_p270_095.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p293_010_to_p270_095.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p293_010_to_p270_095.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p293_010_to_p314_007. People look, but no one ever finds it.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p293_010_to_p314_007.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p293_010_to_p314_007.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p293_010_to_p314_007.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p293_010_to_p314_007.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p293_010_to_p314_007.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p293_010_to_p314_007.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p293_010_to_p374_357. People look, but no one ever finds it.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p293_010_to_p374_357.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p293_010_to_p374_357.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p293_010_to_p374_357.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p293_010_to_p374_357.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p293_010_to_p374_357.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p293_010_to_p374_357.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p293_379_to_p270_095. My husband was fighting for his life.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p293_379_to_p270_095.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p293_379_to_p270_095.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p293_379_to_p270_095.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p293_379_to_p270_095.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p293_379_to_p270_095.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p293_379_to_p270_095.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p293_379_to_p314_007. My husband was fighting for his life.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p293_379_to_p314_007.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p293_379_to_p314_007.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p293_379_to_p314_007.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p293_379_to_p314_007.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p293_379_to_p314_007.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p293_379_to_p314_007.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p293_379_to_p374_357. My husband was fighting for his life.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p293_379_to_p374_357.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p293_379_to_p374_357.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p293_379_to_p374_357.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p293_379_to_p374_357.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p293_379_to_p374_357.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p293_379_to_p374_357.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p314_095_to_p270_095. The money is not really our concern.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p314_095_to_p270_095.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p314_095_to_p270_095.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p314_095_to_p270_095.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p314_095_to_p270_095.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p314_095_to_p270_095.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p314_095_to_p270_095.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p314_095_to_p293_158. The money is not really our concern.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p314_095_to_p293_158.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p314_095_to_p293_158.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p314_095_to_p293_158.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p314_095_to_p293_158.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p314_095_to_p293_158.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p314_095_to_p293_158.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p314_095_to_p374_357. The money is not really our concern.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p314_095_to_p374_357.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p314_095_to_p374_357.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p314_095_to_p374_357.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p314_095_to_p374_357.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p314_095_to_p374_357.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p314_095_to_p374_357.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p314_118_to_p270_095. He would just say it was terrible.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p314_118_to_p270_095.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p314_118_to_p270_095.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p314_118_to_p270_095.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p314_118_to_p270_095.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p314_118_to_p270_095.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p314_118_to_p270_095.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p314_118_to_p293_158. He would just say it was terrible.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p314_118_to_p293_158.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p314_118_to_p293_158.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p314_118_to_p293_158.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p314_118_to_p293_158.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p314_118_to_p293_158.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p314_118_to_p293_158.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p314_118_to_p374_357. He would just say it was terrible.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p314_118_to_p374_357.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p314_118_to_p374_357.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p314_118_to_p374_357.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p314_118_to_p374_357.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p314_118_to_p374_357.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p314_118_to_p374_357.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p374_049_to_p270_095. His condition was serious but stable.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p374_049_to_p270_095.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p374_049_to_p270_095.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p374_049_to_p270_095.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p374_049_to_p270_095.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p374_049_to_p270_095.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p374_049_to_p270_095.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p374_049_to_p293_158. His condition was serious but stable.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p374_049_to_p293_158.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p374_049_to_p293_158.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p374_049_to_p293_158.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p374_049_to_p293_158.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p374_049_to_p293_158.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p374_049_to_p293_158.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p374_049_to_p314_007. His condition was serious but stable.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p374_049_to_p314_007.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p374_049_to_p314_007.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p374_049_to_p314_007.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p374_049_to_p314_007.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p374_049_to_p314_007.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p374_049_to_p314_007.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p374_324_to_p270_095. We did discuss the Lockerbie issue.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p374_324_to_p270_095.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p374_324_to_p270_095.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p374_324_to_p270_095.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p374_324_to_p270_095.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p374_324_to_p270_095.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p374_324_to_p270_095.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p374_324_to_p293_158. We did discuss the Lockerbie issue.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p374_324_to_p293_158.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p374_324_to_p293_158.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p374_324_to_p293_158.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p374_324_to_p293_158.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p374_324_to_p293_158.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p374_324_to_p293_158.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |

p374_324_to_p314_007. We did discuss the Lockerbie issue.

| **Source** | **Referfence** |
| :--- | :--- |
| <audio src="wavs\0.hifi-gan\p374_324_to_p314_007.wav" controls preload></audio> | <audio src="wavs\0.hifi-gan-ref\p374_324_to_p314_007.wav" controls preload></audio> |
| :--- | :--- |

| **VQMIVC** | **VC ($\beta$=1.2e-2)** | **VCT ($\beta$=2.5e-5)** | **VCT ($\beta$=2.5e-5,Cloning)** |
| :--- | :--- | :--- | :--- |
| <audio src="wavs\1.vqmivc\p374_324_to_p314_007.wav" controls preload></audio> | <audio src="wavs\3.vc80.1\p374_324_to_p314_007.wav" controls preload></audio> | <audio src="wavs\6.vc82.1\p374_324_to_p314_007.wav" controls preload></audio> | <audio src="wavs\9.vc82.1-T\p374_324_to_p314_007.wav" controls preload></audio> |
| :--- | :--- | :--- | :--- |
