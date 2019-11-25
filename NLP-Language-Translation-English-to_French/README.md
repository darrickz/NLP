## NLP-Machine-Translation

In this notebook,  several deep neural networks are built functioning as part of an end-to-end machine translation pipeline. This pipeline accepts English text as input and return the French translation.
### Dataset
The dataset for this project is prepared by Udacity from  [`WMT`](http://www.statmt.org/) to contian a small vocabulary, WMT is the most common datasets used for machine translation.
Also the focus of this project is doing translation, some basic preprocesses has been done by Udacity on this data set, including delimiting punctuations  using spaces, and all the text been converted to lowercase. 
#### Dataset info
> 1823250 English words.<br>
> 227 unique English words.<br>
> 10 Most common words in the English dataset:<br>
> "is" "," "." "in" "it" "during" "the" "but" "and" "sometimes"<br>

> 1961295 French words.<br>
> 355 unique French words.<br>
> 10 Most common words in the French dataset:<br>
> "est" "." "," "en" "il" "les" "mais" "et" "la" "parfois"<br>

### Preprocess
1. Tokenize the words into ids
2. Add padding to make all the sequences the same length.

Keras's [`Tokenizer`](https://keras.io/preprocessing/text/#tokenizer) function is used to turn each sentence into a sequence of words ids.<br>
Keras's [`pad_sequences`](https://keras.io/preprocessing/sequence/#pad_sequences) function is used to make all the English sequences have the same length  and all the French sequences have the same length by adding padding to the `end` of each sequence.<br>
#### Preprocessed Dataset info

> Max English sentence length: 15<br>
> Max French sentence length: 21<br>
> English vocabulary size: 199<br>
> French vocabulary size: 345<br>
### Models
In this project, the following four neural network architectures are experimented and the performance are compared:
- Model 1 is a simple RNN: 71%
- Model 2 is a RNN with Embedding: 92%
- Model 3 is a Bidirectional RNN: 74%
- Model 4 is an optional Encoder-Decoder RNN: 70%<br>
- **Final Model: Embedding with stacked Bidirectional RNN: 97%** 

 
