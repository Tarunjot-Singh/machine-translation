# machine-translation



Introduction: 
Despite the fluidity of human language, automated or machine translation is probably one of the most difficult artificial intelligence tasks. Classically, rule-based structures were used for this function, which had been replaced by statistical approaches in the 1990s. More recently, models of deep neural networks have achieved state-of-the-art results in a area aptly called neural machine translation.
For this Project, I will go with Sequence-to- Sequence modelling to achieve the goal.

What is Machine Translation?
Machine translation is the task of automatically converting source text in one language to text in another language.

Data Preprocessing:
It involves the following steps:
1.	All the punctuation is removed as they might not give the accurate result.
2.	Also, Since the data of English and German language is in a single line. It needs to be split on basic of spaces and tab spaces to feed them are independent and dependant variables.
3.	Convert the sentences to lower cases.


Tokenization:
Before feeding the data into the model, it needs to be tokenized. Is the process of tokenizing or dividing a string, a text into a tokens list. One may think of token as parts like a word is a token in a phrase and a phrase is a token in a paragraph.






 

In this tokenizer object is called dataset followed by the fit function which does the job of tokenization. deu_eng is the dictionary and is accessed using slicing operators. Further the length is calculated and stored in a variable. Same process is used for English as well as Dutch sentences.


Model Architecture(Sequence to Sequence):
Multilayer Perceptron neural network models can be used for machine translation, but the models are
constrained by a fixed input sequence in which the output has to be the same length.
 

Seq2seq Working:
Seq2seq takes a sequence of words as input and produces a sequence of words for output. Using recurrent neural network (RNN) it does so. This is because RNN suffers from the problem of vanishing gradient. LSTM is used in the version proposed by Google. It develops the context of the word by taking 2 inputs at each point of time. One from the user and other from its previous output, hence the name recurrent.
It mainly has two parts, i.e. encoder and decoder, and is therefore often called the Network Encoder-Decoder.
Encoder: It uses deep layers of the neural network and transforms the words input into corresponding hidden vectors. Each vector represents the actual word and the word context.
Decoder: The encoder is identical. It takes as input the encoder-generated hidden vector, its own hidden states, and current word to produce the next hidden vector, and finally predicts the next word.



Model Summary:

 
In this model we have the following layers:
Encoding:
•	Embedding and LSTM layer.
Decoding:
•	LSTM layer and dense layer

In several ways LSTMs have an advantage over traditional neural feed-forward networks and RNNs. This is due to their property of selectively recalling patterns for long time periods

 

Predication:
 

The performance of model is impressive, although there are few errors. We can improve the performance further by adding more complex layers into the model. This is the output of first 15 sample of data.
