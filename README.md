### Bigram Language Model for Text Generation

Project Overview
-----------------
This project involves building a Bigram Language Model using TensorFlow to generate text sequences. 
The model processes input text, creates a vocabulary, and encodes words as indices for training.

Key Features
------------
- **Text Preprocessing**:
    - Converts input text to lowercase and removes non-alphabetic characters.
    - Adds special `<start>` and `<end>` tokens to indicate the beginning and end of sentences.
    - Dynamic text loading to manage memory usage, especially for large datasets.
  
- **Vocabulary Creation**:
    - Generates a vocabulary of unique words from the dataset.
    - Encodes words as indices for model input.

- **Dataset Preparation**:
    - Splits data into training and validation sets.
    - Implements a generator to yield word pairs for model training.

- **Model Architecture**:
    - Utilizes an embedding layer, an LSTM layer, and a dropout layer for regularization.
    - Trains the model using categorical cross-entropy loss and Adam optimizer.
  
- **Training and Evaluation**:
    - Includes early stopping and learning rate scheduling to optimize training.
    - Visualizes training and validation accuracy and loss over epochs.

- **Text Generation**:
    - Implements a function to generate text based on a given start word.
    - Evaluates the model’s ability to generate coherent sentences and end them appropriately using the `<end>` token.

Results
-------
- The model is capable of generating text sequences, but with limited coherence.
- It correctly identifies when to end a sentence using the `<end>` token.
- The project highlights the challenges of training language models, including handling large datasets and managing overfitting.

Requirements
------------
- Python 3.x
- Libraries:
    - TensorFlow
    - NumPy
    - Matplotlib
    - Pickle

Usage
-----
1. Preprocess the text data and create a vocabulary.
2. Train the Bigram Language Model using the provided dataset.
3. Generate text sequences using the trained model.

Notes
-----
- The model was trained on a CPU, so training time was longer, and adjustments were made to accommodate hardware limitations.
- The implementation of the `<end>` token was crucial for enabling the model to recognize sentence boundaries.

Disclaimer
----------
This project is provided for educational purposes only. 
The generated text is not intended for real-world use, and the model may produce nonsensical or biased outputs due to its training data.
