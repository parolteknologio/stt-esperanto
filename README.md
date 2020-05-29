# deepspeech-esperanto
Future Deepspeech modell for Esperanto
* https://github.com/mozilla/DeepSpeech
* https://github.com/mozilla/DeepSpeech/blob/master/doc/TRAINING.rst#training-your-own-model


|Dataset|Parameters|Hardware|Results|
|--|--|--|--|
|eo_41h_2019-12-10|python3 DeepSpeech.py --train_files ../eo/clips/train.csv --dev_files ../eo/clips/dev.csv --test_files ../eo/clips/test.csv --automatic_mixed_precision --train_batch_size 16|2 x 1080 Ti 32Gb RAM (leadertelecom)|Time for one Epoch: Total Epochs: WER: File:|
