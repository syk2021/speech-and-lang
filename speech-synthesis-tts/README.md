# Speech Synthesis (TTS) Papers
Compiled with references from https://github.com/wenet-e2e/speech-synthesis-papers, with additions on the TTS front-end side and slight modifications.
Checkout the original list &uarr;!
Like the original list, I keep starred papers (cited for more than 50 times)

## Datasets
* Emotional Speech Synthesis
    * IEMOCAP
 
## TTS Linguistic Front-end
### Text Normalization

### Grapheme-to-Phoneme (G2P)
* [Sequence-to-Sequence Neural Net Models for Grapheme-to-Phoneme Conversion](https://arxiv.org/abs/1506.00196) :stars: (INTERSPEECH 2015)
* [Grapheme-to-Phoneme Conversion using Long Short-Term Memory Recurrent Neural Networks](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43264.pdf) :stars: (IEEE ICASSP 2015)
* [Jointly Learning to Align and Convert Graphemes to Phonemes with Neural Attention Models](https://arxiv.org/abs/1610.06540) :stars: (IEEE SLT 2016)
* [Multitask Sequence-to-Sequence Models for Grapheme-to-Phoneme Conversion](https://www.isca-archive.org/interspeech_2017/milde17_interspeech.html) (INTERSPEECH 2017)
* [Transformer-based Grapheme-to-Phoneme Conversion](https://arxiv.org/abs/2004.06338) (INTERSPEECH 2019)
  
### Phrase Break Prediction
* [Assigning phrase breaks from part-of-speech sequences](https://www.isca-archive.org/eurospeech_1997/black97b_eurospeech.html) :stars: (Eurospeech / INTERSPEECH 1997)
* [Phrase break prediction with bidirectional encoder representations in Japanese text-to-speech synthesis](https://arxiv.org/abs/2104.12395) (INTERSPEECH 2021)

## TTS Acoustic Back-end
### Autoregressive Model
* Tacotron Series <i>End-to-End Speech Synthesis Models by Google</i>
    * Tacotron: [Tacotron: Towards End-to-End Speech Synthesis](https://arxiv.org/abs/1703.10135) :stars: (INTERSPEECH 2017)
    * Tacotron 2: [Natural TTS Synthesis by Conditioning WaveNet on Mel Spectrogram Predictions](https://arxiv.org/abs/1712.05884) :stars: (ICASSP 2018)
    * Non-Attentive Tacotron: [Non-Attentive Tacotron: Robust and Controllable Neural TTS Synthesis Including Unsupervised Duration Modeling](https://arxiv.org/pdf/2010.04301v1.pdf) :stars: (arXiv preprint 2020)
      * Replaces attention mechanism and uses a structure called Gaussian Upsampler & Duration Predictor

### Non-Autoregressive Model
* FastSpeech: [FastSpeech: Fast, Robust, and Controllable Text-to-Speech](https://arxiv.org/abs/1905.09263) (NeurIPS 2019)

### Alignment Study

### Data Efficiency

## Vocoder
A vocoder takes a mel-spectrogram and converts it into an audio file, like a wavfile.

### Autoregressive Model
* WaveNet: [WaveNet: A Generative Model for Raw Audio](https://arxiv.org/abs/1609.03499) (2016)
   * Google DeepMind's post: https://deepmind.google/technologies/wavenet/
* WaveRNN: [Efficient Neural Audio Synthesis](https://arxiv.org/abs/1802.08435) (ICML 2018)
* WaveGAN: [Adversarial Audio Synthesis](https://arxiv.org/abs/1802.04208) (ICLR 2019)
* LPCNet: [LPCNet: Improving Neural Speech Synthesis Through Linear Prediction](https://arxiv.org/abs/1810.11846) (ICASSP 2019)

### Non-Autoregressive Models

## TTS Towards Stylization
### Expressive TTS
If you've ever wondered if system voices could start sounding natural (ie have emotions instead of sounding synthetic) this is the section you want to look at.

### Multispeaker TTS

### New Perspective on TTS

## Voice Conversion
Voice conversion is a relatively new field in TTS.
### ASR & TTS Based
### VAE & Auto-Encoder Based
### GAN Based

## Singing
If you've ever heard of AI covers on YouTube, this is your field of interest. (Kpop AI?)
### Singing Voice Synthesis
### Singing Voice Conversion
