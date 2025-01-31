 Heart-Disease-Prediction-Project-Using-Bagging
This project aims to develop a predictive model utilizing the "Bagging" technique to assess the likelihood of individuals suffering from heart disease. Heart disease is one of the leading causes of death worldwide, necessitating accurate analytical tools to support medical decision-making.


 Project Goals :
- Data Analysis: Explore a dataset containing health and demographic factors.
- Develop an Accurate Model: Use the Bagging technique to improve prediction accuracy.
- Provide Reliable Results: Empower healthcare professionals with data-driven insights.

  Project Contents :
- Data: Contains information about blood pressure, cholesterol levels, and demographic factors (such as age and gender).
- Model: Based on machine learning methods for data analysis and prediction.
 eature Description
The dataset includes a mix of numerical, categorical, and binary features, described as follows:
The dataset includes a mix of numerical, categorical, and binary features, described as follows:
•	Numerical Features:
o	Age: Age of the individual.
o	RestingBP: Resting blood pressure (in mm Hg).
o	Cholesterol: Serum cholesterol levels (in mg/dL).
o	MaxHR: Maximum heart rate achieved.
o	Oldpeak: ST depression induced by exercise relative to rest.
•	Categorical Features:
o	Sex: Gender of the individual (M for Male, F for Female).
o	ChestPainType: Type of chest pain experienced (ATA, NAP, ASY, TA).
o	RestingECG: Resting electrocardiogram results (Normal, ST, LVH).
o	ST_Slope: Slope of the peak exercise ST segment (Up, Flat, Down).
•	Binary Features:
o	FastingBS: Fasting blood sugar > 120 mg/dL (0: No, 1: Yes).
o	ExerciseAngina: Exercise-induced angina (N: No, Y: Yes).
o	HeartDisease: Presence of heart disease (0: No, 1: Yes).

Result :
The model was tested on a smaller dataset (918 samples),
where the proportion of infected individuals was 55%, 
while the proportion of uninfected individuals was 44%, 
indicating a better balance compared to the previous dataset. The model's performance improved significantly,
with the results before tuning illustrated in Figure 4 and after tuning in graph 5


![Screenshot 2025-01-31 190247](https://github.com/user-attachments/assets/8b7a73d4-7e0c-448a-9c22-762bf7a8d30c)

The F1-score of the model before tuning was 0.81, with a precision of 0.82 and recall of 0.81. 
After tuning, these values increased to 0.90 for all three metrics. This improvement demonstrates 
that the model performed better on the more balanced dataset.


Tuning phase :
Hyperparameter tuning is a fundamental process in machine learning, aiming to optimize model performance by systematically identifying the best combination of parameters. In this study, the BaggingClassifier was chosen as the primary model due to its ensemble nature, which combines multiple weak learners to reduce variance and improve stability. Additionally, Bagging’s ability to leverage decision trees as base estimators allows it to capture intricate patterns in the data effectively. These qualities made it a strong candidate for optimizing classification performance in this project. The Grid Search method was employed to fine-tune its parameters. The hyperparameter grid explored values for n_estimators (ranging from 20 to 100),  max_depth (from 5 to 15), and min_samples_split (from 2 to 10). This approach ensured a comprehensive search across possible configurations to achieve optimal performance.

![image](https://github.com/user-attachments/assets/909023f5-9507-4486-a7f4-c607e3cbbf7d)


The results of the Grid Search revealed that the best configuration was max_depth: 5, min_samples_split: 2, and n_estimators: 50. This configuration produced exceptional results on the test set, with an F1 Score, Precision, and Recall all reaching 0.90. Such balanced metrics highlight the model's ability to classify both majority and minority classes with high accuracy. The tuning phase demonstrated a significant improvement in classification performance, achieving Precision, Recall, and F1 Score . The confusion matrix provided further insights into the model's classification ability, showing True Negatives: 66 (correctly classified non-infected cases), False Positives: 11 True Positives: 96 and False Negatives: 11 These results demonstrate the model's proficiency in maintaining a balance between Precision and Recall, making it suitable for applications that require both metrics to be optimized. 


