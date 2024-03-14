# Speech-to-Speech Translation (S2ST) Papers

Speech-to-Speech Translation used to be a cascade of ASR + MT + TTS, but 1) this is largely text-based and 2) results in error propagation, so E2E systems were suggested as an alternative.

E2E systems still compare performance with cascaded systems to understand how well they perform.

## Datasets
Note that speech datasets can either be `read` or `spontaneous`. `Spontaneous` speech is like a day-to-day conversation, `read` is like pre-determined text being read/dictated.

Depending on what style of speech you choose &uarr; and what domains the datasets are on, your finetuning process may yield potentially very different results.

* Fisher Es-En: [Improved speech-to-text translation with the Fisher and Callhome Spanish-English speech translation corpus](https://aclanthology.org/2013.iwslt-papers.14/) (IWSLT 2013)
    * Spanish telephone conversations
    * Remark: I think this is one of the most commonly used datasets in spoken language translation.
* VoxPopuli: [VoxPopuli: A Large-Scale Multilingual Speech Corpus for Representation Learning, Semi-Supervised Learning and Interpretation](https://aclanthology.org/2021.acl-long.80/) (ACL Proceedings 2021)
    * HuggingFace datasets: [facebook/voxpopuli](https://huggingface.co/datasets/facebook/voxpopuli)
    * 1.8K hours of transcribed speeches in 15 languages
    * AND their aligned oral interpretations into 15 target languages
* CVSS: [CVSS Corpus and Massively Multilingual Speech-to-Speech Translation](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.720.pdf) (LREC 2022)
    * HuggingFace datasets: [google/cvss](https://huggingface.co/datasets/google/cvss)
    * S2ST dataset derived from CoVoST2 ST corpus (speech-to-text translation corpus), which is in turn derived from Common Voice
 
## Papers
### End-to-End Speech Translation
* [Sequence-to-Sequence Models Can Directly Translate Foreign Speech](https://arxiv.org/abs/1703.08581) :stars: (INTERSPEECH 2017)
* [Direct speech-to-speech translation with a sequence-to-sequence model: Translatotron](https://arxiv.org/abs/1904.06037) :stars: (INTERSPEECH 2019)
* [Translatotron 2: High-quality direct speech-to-speech translation with voice preservation](https://proceedings.mlr.press/v162/jia22b/jia22b.pdf) (ICML 2022)
    * Replaces attention mechanism with synthesizer (using NAT's Gaussian upsampler)
* [Translatotron 3: Speech to Speech Translation with Monolingual Data](https://arxiv.org/abs/2305.17547) (ICASSP 2024 - to appear)
    * Google Research Blog &rarr; https://blog.research.google/2023/12/unsupervised-speech-to-speech.html
