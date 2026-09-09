# Iris-Flower-Classification
Iris Flower Classification is a machine-learning classification project that predicts the species of an iris flower based on its sepal and petal measurements.
# Iris Flower Classification

## Overview

Iris Flower Classification is a machine-learning classification project that predicts the species of an iris flower based on its sepal and petal measurements.

The project uses the K-Nearest Neighbors (KNN) classification algorithm to classify iris flowers into three species:

* Setosa
* Versicolor
* Virginica

This project is designed for educational, academic, and machine-learning practice purposes.

## Objectives

* Understand the Iris flower dataset.
* Analyze the measurements of different iris species.
* Prepare data for machine learning.
* Train a classification model.
* Predict the species of a new iris flower.
* Evaluate model performance.
* Display classification metrics.
* Visualize the differences between iris species.

## Technologies Used

* Python
* Pandas
* Matplotlib
* Scikit-learn
* K-Nearest Neighbors

## Project Structure

```text
Iris_Flower_Classification/
│
├── README.md
├── iris.csv
├── iris_classification.py
├── requirements.txt
└── iris_classification.png
```

The visualization file `iris_classification.png` is generated when the Python program is executed.

## Dataset

The project uses the Iris flower dataset containing measurements of iris flowers from three different species.

The dataset contains 150 records and five columns.

### Dataset Features

| Feature        | Description                |
| -------------- | -------------------------- |
| `sepal_length` | Length of the flower sepal |
| `sepal_width`  | Width of the flower sepal  |
| `petal_length` | Length of the flower petal |
| `petal_width`  | Width of the flower petal  |
| `species`      | Species of the iris flower |

## Target Variable

The `species` column is the target variable.

The model predicts one of the following three classes:

```text
setosa
versicolor
virginica
```

## Data Preparation

The program loads the dataset using Pandas and separates the input features from the target variable.

The input features are:

```text
sepal_length
sepal_width
petal_length
petal_width
```

The target variable is:

```text
species
```

The dataset is divided into:

* 80% training data
* 20% testing data

A `random_state` of `42` is used to make the split reproducible.

Stratified splitting is used to maintain a balanced representation of each iris species in the training and testing datasets.

## Machine Learning Algorithm

### K-Nearest Neighbors

The project uses the K-Nearest Neighbors classification algorithm with:

```text
Number of Neighbors (k) = 5
```

KNN classifies a new flower by examining the nearest data points in the training dataset and assigning the most common species among those neighboring samples.

KNN is suitable for this project because the Iris dataset is a small classification dataset with numerical features.

## Model Training

The model is trained using the training dataset:

```python
model = KNeighborsClassifier(n_neighbors=5)
model.fit(X_train, y_train)
```

After training, the model predicts the species of flowers in the test dataset.

## Model Evaluation

The model is evaluated using the following metrics.

### Accuracy

Accuracy measures the percentage of test samples that are correctly classified.

The program displays the accuracy as a percentage.

### Classification Report

The classification report provides:

* Precision
* Recall
* F1-score
* Support

for each iris species.

### Confusion Matrix

The confusion matrix shows how many samples from each species were correctly or incorrectly classified.

It helps identify which species are being confused by the model.

## Example Prediction

The project includes an example new flower with the following measurements:

```text
Sepal Length: 5.1
Sepal Width: 3.5
Petal Length: 1.4
Petal Width: 0.2
```

The trained KNN model predicts the species of this flower.

These measurements correspond closely to the characteristics of the `setosa` class in the dataset.

The prediction is displayed when the program is executed.

## Visualization

The project generates a scatter plot using:

* Petal Length
* Petal Width

The flowers are separated according to their species.

This visualization helps demonstrate how the three iris species differ based on petal measurements.

The generated image is saved as:

```text
iris_classification.png
```

## Installation

Make sure Python is installed on your computer.

Open a terminal inside the project directory and install the required libraries:

```bash
pip install -r requirements.txt
```

## Requirements

The project requires the following Python libraries:

```text
pandas
matplotlib
scikit-learn
```

## How to Run

After installing the dependencies, run:

```bash
python iris_classification.py
```

The program will:

1. Load the Iris dataset.
2. Display the first five rows.
3. Display dataset information.
4. Display the distribution of each iris species.
5. Separate features and target values.
6. Split the dataset into training and testing data.
7. Train the KNN classification model.
8. Predict the test dataset.
9. Calculate model accuracy.
10. Display the classification report.
11. Display the confusion matrix.
12. Predict the species of a new flower.
13. Generate the iris classification visualization.

## Output

The program displays:

* First five rows of the dataset
* Dataset information
* Species distribution
* Model accuracy
* Classification report
* Confusion matrix
* Prediction for a new flower

The program also generates:

```text
iris_classification.png
```

## Expected Result

Because the Iris dataset contains well-separated flower classes, KNN can achieve high classification accuracy when trained and tested on the provided data.

The exact accuracy and classification results are calculated when the program is executed.

## Advantages

* Simple and easy-to-understand machine-learning project.
* Suitable for beginners.
* Uses a well-known classification dataset.
* Demonstrates the complete machine-learning workflow.
* Provides multiple model evaluation metrics.
* Includes data visualization.
* Can predict the species of a new flower.

## Limitations

* The dataset contains only four measurements.
* KNN can become computationally expensive with very large datasets.
* The model's performance can be affected by the choice of `k`.
* The project does not include feature scaling, although the Iris features are measured on relatively similar scales.

## Future Improvements

The project can be extended by:

* Comparing KNN with Logistic Regression, Decision Tree, Random Forest, and SVM.
* Testing different values of `k`.
* Adding feature scaling.
* Performing cross-validation.
* Creating an interactive prediction interface.
* Building a web application using Flask or Streamlit.
* Adding more detailed visualizations.
* Saving the trained model for future predictions.

## Disclaimer

This project is created for educational and machine-learning practice purposes. It is not intended for commercial or scientific classification applications without additional validation and testing.
