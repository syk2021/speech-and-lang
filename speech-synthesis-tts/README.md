# Speech Synthesis (TTS) Papers
Compiled with references from https://github.com/wenet-e2e/speech-synthesis-paper, with additions on the TTS front-end side and slight modifications.
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
* [Transformer-based Grapheme-to-Phoneme Conversion](https://arxiv.org/abs/2004.06338) :stars: (INTERSPEECH 2019)
  
### Phrase Break Prediction
* [Assigning phrase breaks from part-of-speech sequences](https://www.isca-archive.org/eurospeech_1997/black97b_eurospeech.html) :stars: (Eurospeech ~~back in the days when INTERSPEECH was Eurospeech~~ / INTERSPEECH 1997)
* [Phrase break prediction with bidirectional encoder representations in Japanese text-to-speech synthesis](https://arxiv.org/abs/2104.12395) (INTERSPEECH 2021)

## TTS Acoustic Back-end
### Autoregressive Model
* Tacotron Series <i>End-to-End Speech Synthesis Models by Google</i>
    * Tacotron :stars:: [Tacotron: Towards End-to-End Speech Synthesis](https://arxiv.org/abs/1703.10135)(INTERSPEECH 2017)
    * Tacotron 2 :stars:: [Natural TTS Synthesis by Conditioning WaveNet on Mel Spectrogram Predictions](https://arxiv.org/abs/1712.05884) (ICASSP 2018)
    * Non-Attentive Tacotron :stars:: [Non-Attentive Tacotron: Robust and Controllable Neural TTS Synthesis Including Unsupervised Duration Modeling](https://arxiv.org/pdf/2010.04301v1.pdf) (arXiv preprint 2020)
      * Replaces attention mechanism and uses a structure called Gaussian Upsampler & Duration Predictor

### Non-Autoregressive Model
* FastSpeech :stars:: [FastSpeech: Fast, Robust, and Controllable Text-to-Speech](https://arxiv.org/abs/1905.09263) (NeurIPS 2019)

### Alignment Study
Attention-based models have their own perks, but not all models using attention are ideal. Find out why here.
* Monotonic attention :stars:: [Monotonic Attention: Online and Linear-Time Attention by Enforcing Monotonic Alignments](https://arxiv.org/abs/1704.00784) (ICML 2017)
    * Recurrent neural network models with attention mechanism have proven to be extremely effective on a wide variety of sequence-to-sequence problems. However, the fact that soft attention mechanism perform a pass over the entire input sequence when producing each element in the output sequence precludes their use in online settings and results in a quadratic time complexity.
    * End-to-End differentiable method for learning monotonic alignments, which at test time, enables computing attention online and in linear time.
* Monotonic Chunkwise Attention :stars:: [Monotonic Chunkwise Attention](https://arxiv.org/abs/1712.05382) (ICLR 2018)
    * Corresponding Google Research article: https://research.google/pubs/monotonic-chunkwise-attention/
* Non-Attentive Tacotron (2020)
    * Replaces attention-based alignment with Duration Predictor, Gaussian Upsampler
* [Location-Relative Attention Mechanisms for Robust Long-Form Speech Synthesis](https://arxiv.org/abs/1910.10288) (ICASSP 2020)
* [One TTS Alignment to Rule Them All](https://ieeexplore.ieee.org/document/9747707) (IEEE ICASSP 2022) 

### Data Efficiency

## Vocoder
A vocoder takes a mel-spectrogram and converts it into an audio file, like a wavfile.

### Autoregressive Model
* WaveNet :stars:: [WaveNet: A Generative Model for Raw Audio](https://arxiv.org/abs/1609.03499) (2016)
   * Google DeepMind's post: https://deepmind.google/technologies/wavenet/
* WaveRNN :stars:: [Efficient Neural Audio Synthesis](https://arxiv.org/abs/1802.08435) (ICML 2018)
* WaveGAN :stars:: [Adversarial Audio Synthesis](https://arxiv.org/abs/1802.04208) (ICLR 2019)
* LPCNet :stars:: [LPCNet: Improving Neural Speech Synthesis Through Linear Prediction](https://arxiv.org/abs/1810.11846) (IEEE ICASSP 2019)

### Non-Autoregressive Models

## TTS Towards Stylization
### Expressive TTS
If you've ever wondered if system voices could start sounding natural (ie have emotions instead of sounding synthetic) this is the section you want to look at.

### Multispeaker TTS

### New Perspective on TTS

## Multilingual and Cross-lingual TTS
One of my fields of interest in TTS, leveraging linguistic knowledge in one field to another.

Most speakers in a TTS database are monolingual, which means that you have to have a synthesizing module for each speaker for each language. This speaker- and language-dependent system poses some barriers. This field studies whether we can overcome these barriers with a single model. This is studied by `multilingual TTS`.

Or what if you don't have enough data in a language that you want to synthesize speech in? Then can you use the resources of a resource-rich language like English to generate speech in another? This is studied by `cross-lingual TTS`.

* [Learning to Speak Fluently in a Foreign Language: Mulitlingual Speech Synthesis and Cross-Language Voice Cloning](https://arxiv.org/abs/1907.04448) (INTERSPEECH 2019)
    * multi-speaker, multilingual text-to-speech (TTS) synthesis based on Tacotron able to produce speech in multiple languages. Able to transfer voices acrsos languages (ie synthesize fluent Spanish speech using an English speaker's voice, without training on any bilingual or parallel examples). Such transfer works for distantly related languages, such as English and Mandarin.
    * audio samples from their paper in Google's GitHub: https://google.github.io/tacotron/publications/multilingual/index.html
* [Phonological Features for 0-shot Multilingual Speech Synthesis](http://www.interspeech2020.org/uploadfile/pdf/Wed-2-11-4.pdf) (INTERSPEECH 2020)
    * Allows generation of intelligible, code-switched speech in new language never seen during training.
* [Cross-lingual Text-to-Speech Synthesis via Domain Adaptation and Perceptual Similarity Regression in Speaker Space](http://www.interspeech2020.org/uploadfile/pdf/Wed-2-11-5.pdf) (INTERSPEECH 2020)
* [End-to-End Code-Switching TTS with Cross-Lingual Language Model](https://ieeexplore.ieee.org/document/9054722) (IEEE ICASSP 2020)
   * `Code Switching` is a term that you will encounter frequently in speech. It refers to the practice of alternating between two or more languages or varieties of languages in conversations. If you know a friend who's bilingual but also bye-lingual :joy: this phenomenon refers to your friend.
   * This paper used a cross-lingual word embedding to encode words of two languages in same embedding space, and allowed words across different languages to share each other's contextual information.
* [Disentangled Speaker and Language Representations using Mutual Information Minimization and Domain Adaptation for Cross-lingual TTS](https://ieeexplore.ieee.org/document/9414226) (IEEE ICASSP 2021)
* [Language-Agnostic Meta-Learning for Low-Resource Text-to-Speech with Articulatory Features](https://aclanthology.org/2022.acl-long.472/) (Proceedings ACL 2022)
* [SANE-TTS: Stable and Natural End-to-End Multilingual Text-to-Speech](https://arxiv.org/abs/2206.12132) (INTERSPEECH 2022)
* Meta Voicebox :stars: : [Voicebox: Text-Guided Multilingual Universal Speech Generation]() (NeurIPS 2023)
   * mono- or cross-lingual zero-shot text-to-speech synthesis
   * cross-lingual style transfer. Beyond using an English audio prompt to generate English speech, Voicebox can also transfer styles across languages.
   * Meta's demolab: https://voicebox.metademolab.com/
* [CrossSpeech: Speaker-independent Acoustic Representation for Cross-lingual Speech Synthesis](https://arxiv.org/pdf/2302.14370.pdf) (IEEE ICASSP 2023)
   * They use metrics like comparative MOS (CMOS) and comparative SMOS (CSMOS) in this paper.


## Voice Conversion
Voice conversion is a relatively new field in TTS.
### ASR & TTS Based
### VAE & Auto-Encoder Based
### GAN Based

## Singing
If you've ever heard of AI covers on YouTube, this is your field of interest. (Kpop AI?)
### Singing Voice Synthesis
### Singing Voice Conversion
