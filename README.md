This project is an effort to build a custom CNN model to classify chest X-ray images into pneumonia, tuberculosis, COVID-19, and normal (healthy) classes. The dataset was compiled from multiple sources and is hosted at https://www.kaggle.com/datasets/imprat/lung-disease-dataset-multiple-sources

A previous version of this project with a binary classification of pneumonia and healthy X-ray images is the Jv1 notebook. The dataset associated with this notebook is hosted at https://www.kaggle.com/datasets/imprat/pneumonia-chest-x-ray-dataset

This project (Jv2) focuses on the development of an automated system for detecting pneumonia from chest X-ray images using a Convolutional Neural Network (CNN). Serious respiratory conditions require prompt and accurate diagnosis to ensure effective treatment and improved patient outcomes.

Objectives:

    To design and implement a CNN model capable of detecting pneumonia from chest X-ray images.
    To train the model using a labeled dataset of chest X-ray images, aiming for high accuracy and robust performance.
    To evaluate the model's performance using various metrics and compare it with existing approaches.

Methodology:

    Data Collection and Preprocessing:
        A dataset of chest X-ray images is collected and preprocessed, including resizing images to a standard size (150x150 pixels) and normalizing pixel values.

    Model Architecture:
        A sequential CNN model is designed with four convolutional layers, each followed by batch normalization and max pooling layers to extract features and reduce spatial dimensions.
        The convolutional layers have 32, 64, 128, and 256 filters, respectively, with ReLU activation functions.
        The model includes a flattened layer to convert 3D feature maps into a 1D vector, followed by three fully connected layers with 512, 256, and 128 neurons, and dropout regularization to prevent overfitting.
        The output layer uses a softmax activation function to classify images into four classes (pneumonia, normal, tuberculosis, and COVID-19).

    Training:
        The model is trained using the Adam optimizer and categorical cross-entropy loss function for 20 epochs with a batch size of 32.
        A learning rate reduction callback is used to adjust the learning rate dynamically based on the validation accuracy.
