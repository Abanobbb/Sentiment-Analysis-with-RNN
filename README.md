# Sentiment-Analysis-with-RNN

Implementation of a recurrent neural network that performs sentiment analysis.

Using an RNN rather than a strictly feedforward network is  accurate since we can include information about the sequence of words.

Here we'll use a dataset of movie reviews, accompanied by sentiment labels: positive or negative.

First, we'll pass in words to an embedding layer. We need an embedding layer because we have tens of thousands of words, so we'll need a more efficient representation for our input data than one-hot encoded vectors. In this case, the embedding layer is for dimensionality reduction, rather than for learning semantic representations.

After input words are passed to an embedding layer, the new embeddings will be passed to LSTM cells. The LSTM cells will add recurrent connections to the network and give us the ability to include information about the sequence of words in the movie review data.

Finally, the LSTM outputs will go to a sigmoid output layer. We're using a sigmoid function because positive and negative = 1 and 0, respectively, and a sigmoid will output predicted, sentiment values between 0-1.

We'll calculate the loss by comparing the output at the last time step and the training label (pos or neg).
