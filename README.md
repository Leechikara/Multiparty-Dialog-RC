# Multiparty-Dialog-RC

Code for the paper:

Challenge Reading Comprehension on Daily Conversations: Passage Completion on Multiparty Dialog

## Requirements
* Python 2.7
* Numpy >= 1.13.3
* Tensorflow >= 1.4.0
* Keras >= 2.0.9

## Datasets

	Our datasets with experimental splits can be found in dialog_rc_data directory
    The original TV show transcripts in json format can be found at https://github.com/emorynlp/character-mining. 
    
* Word embeddings:
	We used Glove vectors with 100 dimentions 
    * glove.6B.zip: [http://nlp.stanford.edu/data/glove.6B.zip](http://nlp.stanford.edu/data/glove.6B.zip)

## Usage
```
    python exp.py --train_file ../dialog_rc_data/Original/Friends_original_sample.train.struct.json 
                   --dev_file ../dialog_rc_data/Original/Friends_original_sample.dev.struct.json 
                   --embedding_file glove.6B.100d.txt
                   --model cnn_lstm_UA_DA --logging_to_file log.txt
                   --save_model model.h5 --stopwords stopwords.txt
```


### Options
* `hidden_size`: default is 32.
* `batch_size`: default is 32.
* `utterance_filters`: default is 50.
* `query_filters`: default is 50.
* `nb_epoch`: default is 100.
* `dropout`: default is 0.2.
* `learning_rate`: default is 0.001.

