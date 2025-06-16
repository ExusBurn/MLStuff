# Iris Flower Classification

## 1. Introduction
The goal of this project is to classify Iris flowers into two species — Setosa and Versicolor — based on sepal and petal measurements.

## 2. Dataset
The Iris dataset consists of 100 rows with 4 features:
- Sepal length
- Sepal width
- Petal length
- Petal width

Each row is labeled with one of three flower species.

## 3. Theory
We use Logistic Regression to perform multi-class classification. This model estimates the probability of each class using a softmax function and learns weights using gradient descent. 

Will also try to use other methodologies(SVM, Naive Bayes) for classification in future.

## 4. Implementation
- Read data using `sklearn.datasets.load_iris()`
- Train/test split: 80/20
- Model: Logistic Regression from `scikit-learn`
- Evaluated accuracy on the test set

## 5. Results : (To be done)
- Test Accuracy:
- Plot: Sepal Length vs Sepal Width (colored by class)

## 6. Conclusion
This basic classification project served as a warm-up for understanding the ML workflow — loading data, training a model, evaluating accuracy, and visualizing results.

## 7. Future Work
- Try other classifiers: KNN, SVM
- Use confusion matrix and precision/recall

