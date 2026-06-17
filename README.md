Iris Flower Classification using SVM

A simple machine learning project that classifies Iris flowers into three species — Setosa, Versicolor, and Virginica — using the Support Vector Machine (SVM) algorithm from scikit-learn.

 Project Overview

This project uses the classic Iris dataset (built into scikit-learn) to:


Explore and understand the dataset structure
Visualize relationships between flower features
Train an SVM model to classify flower species
Evaluate model accuracy with different kernels and parameters


Dataset

The Iris dataset contains 150 samples with the following features:


Sepal Length (cm)
Sepal Width (cm)
Petal Length (cm)
Petal Width (cm)


Each sample belongs to one of three target classes:


0 → Setosa
1 → Versicolor
2 → Virginica


🛠️ Technologies Used


Python
Pandas
Matplotlib
Scikit-learn (SVM, train_test_split, accuracy_score)


 Steps Performed


Data Loading – Loaded the Iris dataset using load_iris() from sklearn.datasets.
DataFrame Creation – Converted the data into a Pandas DataFrame for easier analysis.
Target Mapping – Added target and flower_name columns to label each row with its species.
Data Splitting – Split the dataset by class (Setosa, Versicolor, Virginica) for visualization purposes.
Data Visualization – Plotted scatter graphs comparing:

Sepal Length vs Sepal Width
Petal Length vs Petal Width



Train-Test Split – Divided the data into training (80%) and testing (20%) sets.
Model Training – Trained a Support Vector Classifier (SVM) on the training data.
Model Evaluation – Calculated accuracy using accuracy_score.
Hyperparameter Tuning – Tested the model with:

Regularization parameter C=1
Linear kernel (kernel='linear')





📈 Sample Code

pythonfrom sklearn.svm import SVC
from sklearn.metrics import accuracy_score

model = SVC()
model.fit(X_train, y_train)

y_pred = model.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print(accuracy)

✅ Results


The default SVM model achieved good accuracy on the test set.
Testing with C=1 and a linear kernel helped compare how different settings affect performance.


How to Run


Clone this repository
Install the required libraries:


bash   pip install pandas scikit-learn matplotlib


Run the notebook/script in Jupyter Notebook or any Python IDE


📂 Future Improvements


Try other kernels (rbf, poly) and compare accuracy
Use cross-validation for more reliable accuracy scores
Add a confusion matrix for detailed error analysis



Author: Rahul