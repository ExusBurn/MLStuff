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

We also experimented with Gaussian Naive Bayes, which models each feature using a Gaussian distribution and uses Bayes' Theorem to calculate class probabilities.

## 4. Implementation
- Read data using `pandas.read_csv()`
- Selected 2 classes (Setosa and Versicolor) for binary classification
- Train/test split: 80/20 using manual slicing
- Models used:
  - Logistic Regression from `scikit-learn`
  - Gaussian Naive Bayes from `scikit-learn`
- Performed Exploratory Data Analysis (EDA)
  - Histograms
  - Pair plots
  - Covariance and correlation matrices
- Evaluated model using accuracy and confusion matrix

## 5. Results
- Test Accuracy (both models): 100%
- Confusion matrix confirmed zero misclassifications
- EDA showed that features are linearly separable for the chosen classes

## 6. Conclusion
In this project, we explored the classic Iris flower classification problem using two machine learning models:

- Logistic Regression: A linear model that successfully learned class boundaries and achieved 100% accuracy on our test set.
- Gaussian Naive Bayes: A probabilistic classifier that assumes a normal distribution for each feature; it also achieved 100% accuracy in this case.

### Key Takeaways

- EDA (Exploratory Data Analysis) showed strong feature separability using:
  - Histograms and pair plots for visual intuition.
  - Covariance and correlation matrices to understand numerical relationships.
- Both classes used (Iris-setosa and Iris-versicolor) were linearly separable, making the classification task easier.
- Gaussian Naive Bayes modeled the continuous feature values using:
