# <center> Disentangled Speech Representation Learning for One-Shot Voice Conversion and Cloning </center>

<h2>0. Contents</h2>
1. [Abstract](#abstract)
2. [Samples -- Comparison with other models](#samples-comp)
3. [Other results](#others)

<h2>1. Abstract<a name="abstract"></a></h2>

Learning disentangled speaker and content representations is a fundamental question for speech representation learning.Existing methods typically apply auto-encoder to do the disentanglement while the key is to eliminate the speaker information from the content representation. Our solution is to apply the recent proposed $\beta$-VAE and use the weight $\beta$ for the Kullback-Leibler divergence to restrict the information captured by the content representation. In addition to the evidence lower bound objective, a discriminative objective to regularize the speaker representation has also been imposed. We show quantitatively that with a proper $\beta$, the speaker identity can be largely eliminated from the content representation, with the linguistic information being mostly retained. Qualitative evaluations show that one-shot voice conversion, which is a direct application of the disentangled representation learning, can be achieved with satisfying performance. In addition, we show that texts can be further utilized to regularize the content representation to make it more speaker-invariant and content-related. We do this by introducing a text conditioned prior for content representation, which enables high-quality one-shot voice cloning as a side-product. 


<h2>3. Synthesized samples -- Comparison with other models<a name="samples-comp"></a></h2>

<h3>Below lists the samples that are synthesized for the subjective evaluation.</h3>

LJ003-0305. The provision of more baths was also suggested, and the daily sweeping out of the prison.

| **BVAE-TTS** | **FastSpeech2** | **Glow-TTS** | **Tacotron 2** | **VAENAR-TTS (ours)** |
| :--- | :--- | :--- | :--- | :--- |
| <audio src="wavs\4.BVAE-TTS\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\5.FastSpeech2\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\3.Glow-TTS\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\2.Tacotron2\LJ003-0305.wav" controls preload></audio> | <audio src="wavs\6.VAENAR-TTS\LJ003-0305.wav" controls preload></audio> |
| --- | --- | --- | --- | --- |
