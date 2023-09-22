# Multi-view MidiVAE: Fusing Track- and Bar-view Representations for Long Multi-track Symbolic Music Generation

### *Zhiwei Lin, Jun Chen, Boshi Tang, Binzhu Sha, Jing Yang, Yaolong Ju, Fan Fan, Shiyin Kang, Zhiyong Wu, Helen Meng*

<h2 id = "1">Abstract</h2>
Variational Autoencoders (VAEs)  constitute a crucial component of neural symbolic music generation, among which some works have yielded outstanding results and attracted considerable attention. Nevertheless, previous VAEs still encounter issues with overly long feature sequences and generated results lack contextual coherence, thus the challenge of modeling long multi-track symbolic music still remains unaddressed. To this end, we propose Multi-view MidiVAE, as one of the pioneers in VAE methods that effectively model and generate long multi-track symbolic music.
The Multi-view MidiVAE utilizes the two-dimensional (2-D) representation, OctupleMIDI, to capture relationships among notes while reducing the feature sequences length. Moreover, we focus on instrumental characteristics and harmony as well as global and local information about the musical composition by employing a hybrid variational encoding-decoding strategy to integrate both Track- and Bar-view MidiVAE features. Objective and subjective experimental results on the CocoChorales dataset demonstrate that, compared to the baseline, Multi-view MidiVAE exhibits significant improvements in terms of modeling long multi-track symbolic music. 

<center>
    <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
	<script id="MathJax-script" async
        src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>
    <img style="zoom: 100%;" 
    src="./data/fig/total_arch.jpg">
    <br>
    <div class="caption" style="max-width: 1000px;"> 
    Fig.1: The general schematic of the proposed Inter-SubNet, where "SIL block 1" and "SIL block 2" refer to the first and second SubInter-LSTM block respectively. The "G-norm" denotes group normalization. The Inter-SubNet \(G_{is}\) mainly consists of two stacked SIL blocks and one fully-connected layer. Taking the subband units \(\{\mathbf{b}_i\}_{i=1}^F\) as input, the model \(G_{is}\) generates the final output cIRM \(\mathbf{M}^{r}\) and \(\mathbf{M}^{i}\).
    </div>
</center>




## Without Reverberation

<h3 id = "3"> case 1</h3>

|                          **case 1**                          |                                                              |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Noisy** <br><audio controls><source src="./data/no_reverb/example245/noisy.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Subband model** <br>  <audio controls><source src="./data/no_reverb/example245/Subband_model.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/no_reverb/example245/noisy.jpg" alt="noisy" width="100%" /> | <img src="./data/no_reverb/example245/Subband_model.jpg" alt="baseline" width="100%" /> |
| **Inter-SubNet**<br>  <audio controls><source src="./data/no_reverb/example245/Inter_SubNet.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Clean** <br> <audio controls><source src="./data/no_reverb/example245/clean.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/no_reverb/example245/Inter_SubNet.jpg" alt="proposed" width="100%" /> | <img src="./data/no_reverb/example245/clean.jpg" alt="clean" width="100%" /> |



<h3 id = "3"> case 2</h3>

|                          **case 2**                          |                                                              |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Noisy** <br><audio controls><source src="./data/no_reverb/example110/noisy.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Subband model** <br>  <audio controls><source src="./data/no_reverb/example110/Subband_model.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/no_reverb/example110/noisy.jpg" alt="noisy" width="100%" /> | <img src="./data/no_reverb/example110/Subband_model.jpg" alt="baseline" width="100%" /> |
| **Inter-SubNet**<br>  <audio controls><source src="./data/no_reverb/example110/Inter_SubNet.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Clean** <br> <audio controls><source src="./data/no_reverb/example110/clean.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/no_reverb/example110/Inter_SubNet.jpg" alt="proposed" width="100%" /> | <img src="./data/no_reverb/example110/clean.jpg" alt="clean" width="100%" /> |



<h3 id = "3"> case 3</h3>

|                          **case 3**                          |                                                              |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Noisy**<br/>  <audio controls><source src="./data/no_reverb/example38/noisy.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Subband model**<br/>   <audio controls><source src="./data/no_reverb/example38/Subband_model.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/no_reverb/example38/noisy.jpg" alt="noisy" width="100%" /> | <img src="./data/no_reverb/example38/Subband_model.jpg" alt="baseline" width="100%"/> |
| **Inter-SubNet**  <br/><audio controls><source src="./data/no_reverb/example38/Inter_SubNet.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Clean**  <br/><audio controls><source src="./data/no_reverb/example38/clean.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/no_reverb/example38/Inter_SubNet.jpg" alt="proposed" width="100%" /> | <img src="./data/no_reverb/example38/clean.jpg" alt="clean" width="100%" /> |



<h3 id = "3"> case 4</h3>

|                          **case 4**                          |                                                              |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Noisy**  <br/><audio controls><source src="./data/no_reverb/example213/noisy.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Subband model**  <br/><audio controls><source src="./data/no_reverb/example213/Subband_model.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/no_reverb/example213/noisy.jpg" alt="noisy" width="100%" /> | <img src="./data/no_reverb/example213/Subband_model.jpg" alt="baseline" width="100%" /> |
| **Inter-SubNet**  <br/><audio controls><source src="./data/no_reverb/example213/Inter_SubNet.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Clean**  <br/><audio controls><source src="./data/no_reverb/example213/clean.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/no_reverb/example213/Inter_SubNet.jpg" alt="proposed" width="100%" /> | <img src="./data/no_reverb/example213/clean.jpg" alt="clean" width="100%" /> |







## With Reverberation

<h3 id = "3"> case 1</h3>

|                          **case 1**                          |                                                              |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Noisy** <br><audio controls><source src="./data/with_reverb/example38/noisy.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Subband model** <br>  <audio controls><source src="./data/with_reverb/example38/Subband_model.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/with_reverb/example38/noisy.jpg" alt="noisy" width="100%"/> | <img src="./data/with_reverb/example38/Subband_model.jpg" alt="baseline" width="100%"/> |
| **Inter-SubNet**<br>  <audio controls><source src="./data/with_reverb/example38/Inter_SubNet.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Clean** <br> <audio controls><source src="./data/with_reverb/example38/clean.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/with_reverb/example38/Inter_SubNet.jpg" alt="proposed" width="100%"/> | <img src="./data/with_reverb/example38/clean.jpg" alt="clean" width="100%"/> |



<h3 id = "3"> case 2</h3>

|                          **case 2**                          |                                                              |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Noisy** <br><audio controls><source src="./data/with_reverb/example110/noisy.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Subband model** <br>  <audio controls><source src="./data/with_reverb/example110/Subband_model.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/with_reverb/example110/noisy.jpg" alt="noisy" width="100%" /> | <img src="./data/with_reverb/example110/Subband_model.jpg" alt="baseline" width="100%"/> |
| **Inter-SubNet**<br>  <audio controls><source src="./data/with_reverb/example110/Inter_SubNet.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Clean** <br> <audio controls><source src="./data/with_reverb/example110/clean.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/with_reverb/example110/Inter_SubNet.jpg" alt="proposed" width="100%"/> | <img src="./data/with_reverb/example110/clean.jpg" alt="clean" width="100%"/> |



<h3 id = "3"> case 3</h3>

|                          **case 3**                          |                                                              |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Noisy**  <br/><audio controls><source src="./data/with_reverb/example245/noisy.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Subband model**   <br/><audio controls><source src="./data/with_reverb/example245/Subband_model.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/with_reverb/example245/noisy.jpg" alt="noisy" width="100%"/> | <img src="./data/with_reverb/example245/Subband_model.jpg" alt="baseline" width="100%"/> |
| **Inter-SubNet**  <br/><audio controls><source src="./data/with_reverb/example245/Inter_SubNet.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Clean**  <br/><audio controls><source src="./data/with_reverb/example245/clean.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/with_reverb/example245/Inter_SubNet.jpg" alt="proposed" width="100%"/> | <img src="./data/with_reverb/example245/clean.jpg" alt="clean" width="100%"/> |



<h3 id = "3"> case 4</h3>

|                          **case 4**                          |                                                              |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| **Noisy**  <br/><audio controls><source src="./data/with_reverb/example206/noisy.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Subband model**   <br/><audio controls><source src="./data/with_reverb/example206/Subband_model.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/with_reverb/example206/noisy.jpg" alt="noisy" width="100%"/> | <img src="./data/with_reverb/example206/Subband_model.jpg" alt="baseline" width="100%"/> |
| **Inter-SubNet**  <br/><audio controls><source src="./data/with_reverb/example206/Inter_SubNet.wav" type="audio/wav">Your browser does not support the audio element.</audio> | **Clean**  <br/><audio controls><source src="./data/with_reverb/example206/clean.wav" type="audio/wav">Your browser does not support the audio element.</audio> |
| <img src="./data/with_reverb/example206/Inter_SubNet.jpg" alt="proposed" width="100%"/> | <img src="./data/with_reverb/example206/clean.jpg" alt="clean" width="100%"/> |
