# speech-and-lang
<hr/>

Made this repo on 03.14.2024. because I got tired of looking up papers & datasets while writing a research paper. Hopefully this expedites any ongoing research efforts in my future. This is also a BIG LIST for my own reference haha.

For datasets, I include the paper link + HuggingFace datasets link whenever possible.

For section titles, I include short descriptions of what subsection is (ie what is a vocoder, etc)

Keep in mind that I am also still learning + discovering papers (and yes this means that means this list is not exhaustive!), so please send any requests as a PR through this repo :) 

[Korean] 음성합성 논문 쓰다가 데이터셋 + 논문 찾아보는데 시간이 꽤나 걸리는 것을 발견하여...! 깃허브 리포지토리로 정리했습니다.. 각 subrepo별로 음성/언어 AI 관련 논문 / 데이터셋을 모아두었으나 아직 공부하는 학생이므로 리스트가 아주 완벽하진 않습니다ㅎㅎ 이럴 경우 PR로 추가 부탁드립니다 :)

<hr/>

So, where to begin? What if you're new to AI and want to start learning?
Start by reading this paper by Google, and then move on to each repo of your interest.
Each repo is a starting point in AI research, and each has a README.md that has subsections with each field if you want to dive deeper!
- <b>Attention is All You Need</b>: [Attention is All You Need](https://proceedings.neurips.cc/paper_files/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf) (NeurIPS 2017) &rarr; 110,000+ citations and counting.
  
&uarr; This is basically like the foundation of any of the papers you will see in recent AI research + you'll need to understand this to read any paper that follows in the repos in `speech-and-lang` repo.

Papers with more than 50 citations have :stars: symbols next to them. Read them first!

<hr/>

Sections (Repos)
> Speech Translation (S2ST) Papers

> Speech Synthesis (TTS) Papers

> Speech Recognition (ASR) Papers

> Neural Machine Translation (NMT) Papers

> Speech to Text Translation (S2TT) Papers

> Pretrained Language Models

> Speech Processing Toolkits

<hr/>

Also, just including some interesting (and free) resources that I used to study Speech & Language AI:
* [Stanford CS224N Natural Language Proceessing](https://web.stanford.edu/class/cs224n/)
* [Speech and Language Processing (also from Stanford)](https://web.stanford.edu/~jurafsky/slp3/)
    * If you want to get a textbook-style intro to NLP & its applications this is your go to
    * Includes Machine Translation, Question Answering, Chatbots & Dialogues, Automatic Speech Recognition & Text-to-Speech
    * Speech & Language Processing also includes a lot of cited papers at the end, so care to take a look!
* HuggingFace Courses
    * [<b>NLP</b>](https://huggingface.co/learn/nlp-course/chapter1/1)
    * [<b>Audio</b>](https://huggingface.co/learn/audio-course/chapter0/introduction)
 
<hr/>

Interesting libraries & resources if you are a speech enthusiast.
* <b>librosa</b> &rarr; you can graph mel-spectrograms on your own with librosa.ex files. [Here's](https://librosa.org/doc/main/generated/librosa.feature.melspectrogram.html) a helpful tutorial on this.
* <b>gradio</b> &rarr; making audio demonstrations with an interface
* <b>torchaudio</b> &rarr; [This](https://pytorch.org/audio/stable/index.html) is the torchaudio documentation, and also has interesting tutorials on the topics below &darr;
    * It includes ASR / CTC / CTC Decoder / CUDA CTC Decoder / DSP / Dataset / Forced Alignment / I/O / Pipelines / Preprocessing / RNNT / Source Separation / Speech / Speech Enhancement / StreamReader / StreamWrite / TTS (Text-to-Speech) / wav2vec2
* <b>WandB</b> &rarr; You will need this to train & find hyperparameters. Alternatively, you can use Tensorboard.
* <b>Google Colab</b> &rarr; can use their GPU to train but you will probably need to upgrade to Pro for more compute.
* <b>[NeMo Tutorials](https://nvidia.github.io/NeMo/)</b> &rarr; Nvidia also has helpful resources on speech processing.

<hr/>

Last note:
If you ever need to use HuggingFace datasets, set streaming=True and do next(iter(dataset_var)).
This will save your computer from running out of local memory :innocent: and yes, if you download VoxPopuli, CommonVoice, FLEURS, etc you will eventually run out of memory... (~~This is coming from experience~~)
