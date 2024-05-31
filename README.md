# FAQ Chatbot with TensorFlow

This repository contains a TensorFlow-based FAQ chatbot that employs a Long Short-Term Memory (LSTM) model to generate responses to user queries. Here's a breakdown of the code:

## Model Architecture

The model consists of the following layers:

- **Embedding Layer**: This layer converts word indices into dense vectors of a fixed size. It helps represent words in a continuous vector space.
  
- **LSTM Layer**: LSTM (Long Short-Term Memory) networks are a type of recurrent neural network (RNN) architecture capable of learning long-term dependencies. In this model, LSTM captures the temporal dependencies in the sequence of words, which is crucial for understanding the context of sentences.
  
- **Dense Layer**: The dense layer is a fully connected layer that outputs a probability distribution over the vocabulary for the next word prediction. It utilizes a softmax activation function to ensure that the output values are in the range [0, 1] and sum up to 1, representing probabilities.

## Training

The model is trained using the categorical cross-entropy loss function and the Adam optimizer. The training data consists of sequences of words from the FAQ dataset, with each sequence serving as input, and the target being the next word in the sequence. The model learns to predict the next word based on the context provided by the preceding words.

## Prediction

The prediction loop demonstrates how to use the trained model to generate responses. It takes an input text, tokenizes it using a tokenizer trained on the FAQ dataset, pads it to the maximum sequence length observed during training, and then uses the model to predict the next word. This predicted word is appended to the input text, and the process repeats for a specified number of iterations, generating a sequence of words that form the bot's response.

## Usage

The provided code snippet illustrates how to train the model and use it for prediction. It includes steps such as data preprocessing, model compilation, training, and prediction. Before running the code, ensure that you have TensorFlow and other required dependencies installed.
