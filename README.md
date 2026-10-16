# Machine Learning Tasks Collection

This repository contains three machine learning projects implemented in
Python using Jupyter Notebooks. The tasks cover **credit default
prediction**, **handwritten character recognition**, and **heart disease
prediction**.

## Projects

### 2. Handwritten Character Recognition

**Folder:** `Handwritten Character Recognition`

This project uses a **Convolutional Neural Network (CNN)** to recognize
handwritten characters/digits from 28×28 pixel images.

#### Dataset

-   File: `train.csv`
-   Records: 42,000
-   Input features: 784 pixel values
-   Image size: 28×28
-   Number of classes: 10

#### Methodology

-   Loaded the image dataset using Pandas
-   Separated labels and pixel features
-   Reshaped the 784 pixels into 28×28 grayscale images
-   Normalized pixel values to the range 0--1
-   Encoded the target labels using one-hot encoding
-   Split the dataset into training and testing sets
-   Built a CNN using:
    -   Convolutional layers
    -   Max Pooling layers
    -   Flatten layer
    -   Dense layer
    -   Dropout
    -   Softmax output layer
-   Trained the model for 10 epochs
-   Evaluated the model using test accuracy and classification metrics
-   Generated a confusion matrix and sample predictions
-   Saved the trained model as `handwritten_character_cnn.keras`

#### Results

  Metric            Result
  --------------- --------
  Test Accuracy     99.01%
  Test Loss         0.0369
  Test Samples       8,400

The model achieved approximately **99% test accuracy** after 10 epochs.

## Important Notes

-   The notebooks contain the complete data preprocessing, model
    training, evaluation, and prediction workflow.
-   Results can vary slightly when the notebooks are retrained in a
    different environment or with different library versions.
-   The disease prediction project is an educational machine learning
    project and should not be used as a substitute for professional
    medical diagnosis.
-   The credit scoring model is also intended for educational purposes
    and should not be treated as a production financial decision system
    without further validation.

## Author

**Muhammad Khursheed**

**BSCS --- Minhaj University Lahore**

## License

This project is intended for educational and academic purposes.
