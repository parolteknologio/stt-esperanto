# deepspeech-esperanto
Future Deepspeech modell for Esperanto
* https://github.com/mozilla/DeepSpeech
* https://deepspeech.readthedocs.io/en/v0.7.1/TRAINING.html

|Dataset|Parameters|Hardware|Results|
|--|--|--|--|
|eo_41h_2019-12-10|python3 DeepSpeech.py --train_files ../eo/clips/train.csv --dev_files ../eo/clips/dev.csv --test_files ../eo/clips/test.csv --automatic_mixed_precision --train_batch_size 16|2 x 1080 Ti 32Gb RAM (leadertelecom)|Time for one Epoch: 3h <br> Total Epochs:3 <br> nefinita|

> wget https://voice-prod-bundler-ee1969a6ce8178826482b88e843c335139bd3fb4.s3.amazonaws.com/cv-corpus-4-2019-12-10/eo.tar.gz

> sudo apt-get install sox libsox-fmt-mp3

> python3 DeepSpeech.py --train_files ../eo/clips/train.csv --dev_files ../eo/clips/dev.csv --test_files ../eo/clips/test.csv --automatic_mixed_precision --train_batch_size 16 -- epochs 5

> scp -r  usergpu@185.x.x.x:/home/usergpu/.local/share/deepspeech/checkpoints/ /Users/nomo/

Todo:
- run ssh process in background (background + disown process)
- create kenlm language model (scorer). https://tiefenauer.github.io/blog/wiki-n-gram-lm/ https://github.com/kpu/kenlm
