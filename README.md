# Esperanto STT
* [Scorer](https://github.com/parolteknologio/stt-esperanto/tree/master/scorer) KenLM Scorer in Esperanto
* [Deepspeech/Coqui AI models](https://github.com/parolteknologio/stt-esperanto/tree/master/deepspeech-coqui) - find and Download .tflite models
* [Colab Notebooks](https://github.com/parolteknologio/stt-esperanto/tree/master/colab-notebooks)

Using deepspeech/coqui ai and the common voice dataset
* https://github.com/coqui-ai/STT
* https://stt.readthedocs.io/en/latest/
* Tim jam kreis sistemon en esperantto: https://gitlab.com/54696d21

Tools/Iloj

* Ilo por krei subtekstojn en Esperanto [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/parolteknologio/stt-esperanto/blob/master/colab-notebooks/Subtekstoj_en_Esperanto.ipynb)

## eblaj datumfontoj

|Datumaro|versio|grandeco|permesilo|
|--|--|--|--|
|[Common Voice](https://commonvoice.mozilla.org/eo/datasets)|CV Corpus 7.0 |17 GB 748 h|CC 0|
|[tatoeba](https://tatoeba.org/epo/sentences/search?query=&from=epo&to=none&user=&orphans=no&unapproved=no&has_audio=yes&tags=&list=&native=&trans_filter=limit&trans_to=und&trans_link=&trans_user=&trans_orphan=&trans_unapproved=&trans_has_audio=&sort=relevance&sort_reverse=)|03.06.20|4 063 audio files|CC-BY|
|[lingualibre](https://lingualibre.org/wiki/Help:Download_from_LinguaLibre)|03.06.20|425 MB|CC BY-SA|


## experiments so far

|datumaro|parametroj|GPU|rezultoj|
|--|--|--|--|
|eo_41h_2019-12-10|?|2 x 1080 Ti 32Gb RAM (leadertelecom)| WER 0.5|
|eo_844h_2021-07-21|english checkpoints, n_depth 2048, dropout_rate 0.3, learning_rate 0.0001  [details](https://github.com/parolteknologio/stt-esperanto/blob/master/deepspeech-coqui/common-voice-corpus-7/2048-transfer-from-english.txt)|Google Colab Pro Plus| WER 24,7% (test was part of train dataset) [download](https://github.com/parolteknologio/stt-esperanto/tree/master/deepspeech-coqui/common-voice-corpus-7)|


## To do:
- run ssh process in background next time (background + disown process)
- experiment with different data tables e.g. ignore sentences with one no-vote
- extract the [Tatoeba](https://tatoeba.org/epo/sentences/search?query=&from=epo&to=none&user=&orphans=no&unapproved=no&has_audio=yes&tags=&list=&native=&trans_filter=limit&trans_to=und&trans_link=&trans_user=&trans_orphan=&trans_unapproved=&trans_has_audio=&sort=relevance&sort_reverse=) corpus with the script from https://github.com/DanBmh/deepspeech-german
- Extract lingua libre files https://github.com/mozilla/DeepSpeech/blob/master/bin/import_lingua_libre.py
- create kenlm language model (scorer). https://tiefenauer.github.io/blog/wiki-n-gram-lm/ https://github.com/kpu/kenlm


