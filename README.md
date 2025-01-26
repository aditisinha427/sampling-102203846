# Sampling Techniques and Model Performance Analysis
Objective
The goal of this assignment was to evaluate the impact of different sampling techniques on the performance of various machine learning models. By experimenting with these techniques, we aimed to understand how data preparation influences model accuracy and generalization.

Dataset
The dataset used in this analysis is the credit card fraud detection dataset, where the target variable (Class) represents whether a transaction is fraudulent (1) or not (0). The data is highly imbalanced, necessitating careful handling to ensure fair evaluation of models.

Sampling Techniques
To ensure diversity in data preparation, we implemented the following sampling techniques:

Simple Random Sampling: Randomly selects samples, maintaining no specific structure.
Systematic Sampling: Samples every second row (or every nth row).
Stratified Sampling: Maintains the proportion of fraud and non-fraud cases in the sampled data.
Cluster Sampling: Focuses on a specific feature (V1 in this case) to create clusters and sample from them.
Bootstrap Sampling: Samples with replacement, creating a dataset with repeated instances.

Machine Learning Models
The following models were chosen for their diversity and performance:

Logistic Regression: A simple and interpretable linear model.
Decision Tree: A tree-based model capturing non-linear relationships.
Random Forest: An ensemble model known for reducing overfitting.
Support Vector Machine (SVM): Effective for small datasets with a clear margin of separation.
K-Nearest Neighbors (KNN): A non-parametric, instance-based learning algorithm.

Methodology
The dataset was balanced using undersampling to address class imbalance.
Each sampling technique was applied to create subsets of the data.
Models were trained and tested using an 80-20 train-test split for each subset.
Accuracy scores were calculated for every combination of sampling technique and model.

Results
The results of the analysis were saved to a CSV file (sampling_results.csv) for further evaluation. Accuracy scores for each sampling technique and model were also printed to the console for real-time monitoring.

Key Observations
Simple Random Sampling:
Provided baseline performance metrics.
May lead to poor representation of minority classes due to randomness.
Systematic Sampling:
Ensured even distribution of samples but may miss patterns in the data if the step size aligns with periodic patterns.
Stratified Sampling:
Maintained the proportion of fraud and non-fraud transactions, leading to consistent model performance.
Cluster Sampling:
Performance depended on how well the clusters represented the dataset. If the chosen feature didn't capture meaningful clusters, the accuracy was inconsistent.
Bootstrap Sampling:
Worked well for ensemble methods like Random Forest, which benefit from variance reduction due to repeated sampling.

Conclusion
This assignment highlighted the importance of data sampling in machine learning workflows. Sampling techniques significantly influence model performance, especially for imbalanced datasets. Properly chosen techniques, such as stratified sampling, help preserve the dataset's characteristics, leading to better generalization of models.



