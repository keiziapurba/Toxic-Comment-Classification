# Toxic-Comment-Classification

![Toxic Comment Classification]()

## Table of Contents:
- [Introduction](#introduction)
- [Preprocessing](#preprocessing)
- [Model Architecture](#model-architecture)
- [Model Training](#model-training)
- [Model Evaluation](#model-evaluation)
- [Deployment](#deployment)
- [Usage](#usage)
- [Contributing](#contributing)

## Introduction

The **Toxic Comment Classification** project focuses on developing a deep learning model to classify comments as toxic or non-toxic based on their content. The model aims to automatically identify and flag comments that contain offensive, disrespectful, or harmful language, helping maintain a safer and more inclusive online environment.

## Preprocessing

The preprocessing step involves transforming the raw comment data into a format suitable for model training. The following steps are performed:

- **Text Vectorization**: The comments are tokenized and converted into sequences of integers using the TextVectorization layer from TensorFlow. This layer creates a vocabulary of words and assigns each word a unique integer. The comments are then encoded as sequences of these integers.
- **Dataset Creation**: The preprocessed data is converted into a TensorFlow Dataset object, which is an efficient way to feed data to the model during training. The dataset is shuffled, batched, and pre-fetched to optimize training performance.

## Model Architecture

The model architecture is as follows:

- **Embedding Layer**: An embedding layer is added to learn the representation of words in a low-dimensional space. It maps each word index to a dense vector representation, capturing the meaning and context of words.
- **Bidirectional LSTM Layer**: A bidirectional LSTM layer is used to capture the sequential information and dependencies within the comments. It processes the comments in both forward and backward directions, enhancing the model's understanding of the context.
- **Fully Connected Layers**: Several fully connected layers are added to extract relevant features from the sequential representation. These layers perform nonlinear transformations, helping the model learn complex patterns and relationships.
- **Output Layer**: The final layer is a dense layer with a sigmoid activation function. It outputs the classification probabilities for each toxic category.

## Model Training

The model is trained using the compiled model architecture and the training dataset. The following steps are involved:

- **Model Compilation**: The model is compiled with the binary cross-entropy loss function and the Adam optimizer.
- **Training**: The model is trained using the training dataset for a specified number of epochs. The validation dataset is used to monitor the model's performance during training.

## Model Evaluation

The trained model is evaluated using various metrics to assess its performance. The following metrics are calculated:

- **Precision**: Measures the model's ability to correctly identify true positive instances.
- **Recall**: Measures the model's ability to correctly identify all positive instances.
- **Accuracy**: Measures the overall accuracy of the model's predictions.

## Deployment

The model is deployed using the Gradio library, which provides a user-friendly graphical interface. The following steps are involved:

- **Model Saving**: The trained model is saved to a file for future use.
- **Model Loading**: The saved model is loaded for deployment.
- **Comment Scoring**: A function is defined to score a given comment using the loaded model. The function preprocesses the comment, passes it through the model, and generates toxicity predictions.
- **Gradio Interface**: A Gradio interface is created, allowing users to enter comments and view the model's toxicity predictions.

## Usage

To use the project code, follow these steps:
1. Install the required dependencies mentioned in the project code.
2. Load the dataset and preprocess the comments using the provided code.
3. Define and compile the model architecture.
4. Train the model using the training dataset.
5. Evaluate the model using the validation dataset to assess its performance.
6. Save the trained model to a file for future use.
7. Load the saved model for deployment.
8. Define a function to score a comment using the loaded model.
9. Use the Gradio library to create a graphical user interface (GUI) for users to interact with the model and obtain toxicity predictions.
10. Launch the Gradio interface and share it with others.


## Contributing

Contributions to the project are welcome! If you have any ideas, suggestions, or improvements, feel free to submit a pull request or open an issue.

