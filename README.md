# Predicting-Survival-From-The-Titanic-Using-Logistical-Regression
a machine learning project aimed at predicting the survival of passengers on the Titanic ship disaster.


the data was taken from this source : https://github.com/datasciencedojo/datasets/blob/master/titanic.csv

# Data Preprocessing
## Loading the Data: The code starts by loading the Titanic dataset from a CSV file named titanic (2).csv.
## Handling Missing Values: The code drops the 'Cabin' column as it has a large number of missing values, and then drops any rows with missing values.
## Encoding Categorical Features: The code performs the following encoding techniques:
1- 'Sex' column is encoded using one-hot encoding, creating two new columns 'Sex_female' and 'Sex_male'.


2- 'Ticket' column is encoded using Label Encoding.


3- 'Embarked' column is encoded using Label Encoding.


## Dropping Unnecessary Columns: The 'Name' column is dropped as it is not expected to be a useful feature for the prediction task.


![image](https://github.com/user-attachments/assets/eb15c9c2-83dc-4144-a4ce-f2adba911cbf)

# Exploratory Data Analysis
The code includes some basic exploratory data analysis, such as printing the first few rows of the dataset, the information about the dataset, and the descriptive statistics.

![image](https://github.com/user-attachments/assets/7b92f9c7-718a-4b44-9a0d-b46639a39c32)


![image](https://github.com/user-attachments/assets/77ab7ad3-fcf4-4758-94b8-7045ff7d5561)

# Model Training and Evaluation

![image](https://github.com/user-attachments/assets/58c3baaf-63c1-4403-80aa-af380430d719)


![image](https://github.com/user-attachments/assets/64911b8a-b33e-4932-8430-ee82d1a66cc7)

The confusion matrix presented in the image provides valuable insights into the model's performance. The high number of 295 instances correctly classified as 0 (predicted 0, actual 0) suggests that the model is effectively identifying the majority class. This is a positive indication, as accurately predicting the negative class is often crucial for many real-world applications.

Additionally, the 156 instances correctly classified as 1 (predicted 1, actual 1) demonstrate the model's ability to identify the positive class with reasonable accuracy. While the number of false negatives (49) and false positives (69) indicates room for improvement, the overall performance seems promising, especially considering the inherent challenges in predicting such a complex and sensitive problem like Titanic passenger survival.

The visualization of the confusion matrix allows for easy interpretation and provides a clear understanding of the model's strengths and weaknesses. This information can be used to further refine the model, potentially by exploring additional features, adjusting hyperparameters, or incorporating more advanced techniques to enhance the overall predictive accuracy.

![image](https://github.com/user-attachments/assets/7672abbe-c107-4325-b966-7035164090d8)

The classification report presented in the image provides several encouraging metrics that demonstrate the model's strong performance:

Precision: The model achieves a high precision score of 0.81, indicating that a large proportion of the instances it identifies as the positive class (i.e., survived) are indeed actual survivors. This is a positive result, as it suggests the model is making reliable predictions and minimizing the number of false positives.
Recall: The recall score of 0.86 is also commendable, meaning the model is able to correctly identify a high percentage of the actual survivors. This is an important metric, as it reflects the model's ability to capture the positive class effectively.
F1-score: The F1-score, which combines precision and recall, stands at 0.83, which is a strong overall performance metric. This well-balanced score indicates that the model is achieving a good balance between accurately identifying survivors and minimizing misclassifications.
These metrics, taken together, demonstrate the model's solid predictive capabilities on the Titanic survival problem. The high precision, recall, and F1-score suggest that the model is making reliable and accurate predictions, which is crucial for real-world applications where correctly identifying survivors is of paramount importance.


![image](https://github.com/user-attachments/assets/8c5dd54f-2d74-4da6-a996-6b302feba45b)


The testing results shown in this image are quite positive and demonstrate the model's strong performance on the testing data:

Testing Accuracy: The model achieves an accuracy score of 0.80 on the testing data, which is a respectable result. An accuracy of 0.80 means the model is correctly predicting the survival status of 80% of the passengers in the testing set.
Confusion Matrix: The confusion matrix provides additional insights into the model's performance. The large number of true negatives (74) and true positives (40) indicates that the model is effectively identifying both the passengers who did not survive and those who did survive.
Balanced Errors: The confusion matrix also shows a relatively balanced distribution of errors, with 23 false negatives (passengers predicted to not survive but who actually survived) and 6 false positives (passengers predicted to survive but who actually did not). This suggests the model is not heavily biased towards one class or the other, which is a desirable property.
Visual Representation: The visual representation of the confusion matrix provides a clear and intuitive way to interpret the model's performance. The color-coding and label placement make it easy to understand the distribution of true positives, true negatives, false positives, and false negatives.
Overall, these results indicate that the model is performing well on the testing data and is able to accurately predict the survival status of Titanic passengers. The combination of a good accuracy score and a well-balanced confusion matrix suggests the model has been trained effectively and is suitable for real-world deployment, provided the training and testing data are representative of the target population.

