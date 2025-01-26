# Sampling Techniques and Model Performance Analysis
# Objective
The goal of this assignment was to evaluate the impact of different sampling techniques on the performance of various machine learning models. By experimenting with these techniques, we aimed to understand how data preparation influences model accuracy and generalization.

# Dataset
The dataset used in this analysis is the credit card fraud detection dataset, where the target variable (Class) represents whether a transaction is fraudulent (1) or not (0). The data is highly imbalanced, necessitating careful handling to ensure fair evaluation of models.

# Sampling Techniques
To ensure diversity in data preparation, we implemented the following sampling techniques:

Simple Random Sampling: Randomly selects samples, maintaining no specific structure. <br>
Systematic Sampling: Samples every second row (or every nth row). <br>
Stratified Sampling: Maintains the proportion of fraud and non-fraud cases in the sampled data. <br>
Cluster Sampling: Focuses on a specific feature (V1 in this case) to create clusters and sample from them. <br>
Bootstrap Sampling: Samples with replacement, creating a dataset with repeated instances. <br>

# Machine Learning Models
The following models were chosen for their diversity and performance: <br>

Logistic Regression: A simple and interpretable linear model. <br>
Decision Tree: A tree-based model capturing non-linear relationships. <br>
Random Forest: An ensemble model known for reducing overfitting. <br>
Support Vector Machine (SVM): Effective for small datasets with a clear margin of separation. <br>
K-Nearest Neighbors (KNN): A non-parametric, instance-based learning algorithm. <br>

# Methodology
The dataset was balanced using undersampling to address class imbalance.<br>
Each sampling technique was applied to create subsets of the data. <br>
Models were trained and tested using an 80-20 train-test split for each subset. <br>
Accuracy scores were calculated for every combination of sampling technique and model. <br>

# Results
The results of the analysis were saved to a CSV file (sampling_results.csv) for further evaluation. Accuracy scores for each sampling technique and model were also printed to the console for real-time monitoring.

# Key Observations
Simple Random Sampling: <br>
Provided baseline performance metrics. <br>
May lead to poor representation of minority classes due to randomness. <br>
Systematic Sampling: <br>
Ensured even distribution of samples but may miss patterns in the data if the step size aligns with periodic patterns. <br>
Stratified Sampling:
Maintained the proportion of fraud and non-fraud transactions, leading to consistent model performance. <br>
Cluster Sampling: <br>
Performance depended on how well the clusters represented the dataset. If the chosen feature didn't capture meaningful clusters, the accuracy was inconsistent. <br>
Bootstrap Sampling: <br>
Worked well for ensemble methods like Random Forest, which benefit from variance reduction due to repeated sampling. <br>

# Conclusion
This assignment highlighted the importance of data sampling in machine learning workflows. Sampling techniques significantly influence model performance, especially for imbalanced datasets. Properly chosen techniques, such as stratified sampling, help preserve the dataset's characteristics, leading to better generalization of models.



