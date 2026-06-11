# Iris Flower Classification with K-Nearest Neighbors (KNN)

This project demonstrates a machine learning workflow for classifying iris flowers into three species (setosa, versicolor, and virginica) based on four features: sepal length, sepal width, petal length, and petal width. The classification is performed using the K-Nearest Neighbors (KNN) algorithm.

## Project Steps

The project is implemented in a Jupyter Notebook (`project2.ipynb`) and follows these key steps:

### 1. Load & Explore the Data

- The famous Iris dataset is loaded from `sklearn.datasets`.
- The dataset is explored to understand its structure, including:
  - The shape of the data (number of samples and features).
  - The names of the three flower species (classes).
  - The names of the four features.
  - The balance of the classes in the dataset.

### 2. Feature Scaling

- To ensure that all features contribute equally to the model's predictions, the feature values are standardized.
- `StandardScaler` from scikit-learn is used to scale the features to have a mean of 0 and a standard deviation of 1.

### 3. Train/Test Split

- The dataset is split into a training set and a testing set.
- 80% of the data is used for training the model, and 20% is reserved for testing its performance.

### 4. Finding the Optimal 'k' with the Elbow Method

- The performance of the KNN algorithm is sensitive to the choice of the number of neighbors ('k').
- The "Elbow Method" is used to find the optimal 'k'. This involves:
  - Training and testing the KNN model for a range of 'k' values (from 1 to 30).
  - Plotting the error rate for each 'k'.
  - Selecting the 'k' value where the error rate is at its minimum, which appears as an "elbow" in the plot.

### 5. Training the Final Model

- A new KNN model is trained on the entire training set using the optimal 'k' value found in the previous step.

### 6. Evaluating the Model

- The performance of the final model is evaluated on the unseen test data.
- The evaluation includes:
  - **Accuracy**: The proportion of correctly classified flowers.
  - **Confusion Matrix**: A table that visualizes the performance of the classification model by showing the counts of true and false predictions for each class.
  - **Classification Report**: A detailed report that includes precision, recall, and F1-score for each class.
  - **Weighted F1 Score**: The weighted average of the F1-scores for each class.

## How to Run the Project

1.  Ensure you have Python and Jupyter Notebook installed.
2.  Install the required libraries:
    ```bash
    pip install numpy pandas matplotlib seaborn scikit-learn
    ```
3.  Open and run the `project2.ipynb` notebook.
