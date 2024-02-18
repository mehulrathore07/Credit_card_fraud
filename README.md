# Credit_card_fraud

# Introduction
Credit Card Frauds are the cases of using someone else's credit cards for financial transactions without the information of the card owner. Credit Cards were made available inorder for the people to increase their buying power, it is an agreement with your bank that lets the user use the money lended by the bank in exchange for the repayment of this lended money on the due date or incur interest charges. With the rise in the e-commerce and the recent boom of OTT platforms during the Coronavirus Pandemic, use of credit cards has risen exponentially along with other payment processes. As all the things in the nature are binary, cases of credit card frauds has also achieved high numbers. Thus, building automated models for such a rising problem statement is necessary and AI - ML is the key for it!

# Aim
- To classify whether a credit card transaction is fradulent or genuine and handle unbalanced dataset.
- It is a binary classification problem with highly unbalanced data.

# Dataset Information
The datasets contains transactions made by credit cards in September 2013 by european cardholders. This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation.

Due to confidentiality issues, there are not provided the original features and more background information about the data.

Features V1, V2, ... V28 are the principal components obtained with PCA; The only features which have not been transformed with PCA are Time and Amount. Feature Time contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature Amount is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature Class is the response variable and it takes value 1 in case of fraud and 0 otherwise.

# Anomaly Detection Algorithms
Anomaly detection algorithms are used to identify patterns or instances that deviate from normal behavior within a dataset. These anomalies, also known as outliers or novelties, can represent critical information such as fraudulent transactions, equipment malfunctions, or cybersecurity threats. Here are some commonly used anomaly detection algorithms

- Isolation Forest Algorithm: One of the newest techniques to detect anomalies is called Isolation Forests. The algorithm is based on the fact that anomalies are data points that are few and different. As a result of these properties, anomalies are susceptible to a mechanism called isolation.

This method is highly useful and is fundamentally different from all existing methods. It introduces the use of isolation as a more effective and efficient means to detect anomalies than the commonly used basic distance and density measures. Moreover, this method is an algorithm with a low linear time complexity and a small memory requirement. It builds a good performing model with a small number of trees using small sub-samples of fixed size, regardless of the size of a data set.

Typical machine learning methods tend to work better when the patterns they try to learn are balanced, meaning the same amount of good and bad behaviors are present in the dataset.

How Isolation Forests Work The Isolation Forest algorithm isolates observations by randomly selecting a feature and then randomly selecting a split value between the maximum and minimum values of the selected feature. The logic argument goes: isolating anomaly observations is easier because only a few conditions are needed to separate those cases from the normal observations. On the other hand, isolating normal observations require more conditions. Therefore, an anomaly score can be calculated as the number of conditions required to separate a given observation.

The way that the algorithm constructs the separation is by first creating isolation trees, or random decision trees. Then, the score is calculated as the path length to isolate the observation.

- Local Outlier Factor(LOF) Algorithm: The LOF algorithm is an unsupervised outlier detection method which computes the local density deviation of a given data point with respect to its neighbors. It considers as outlier samples that have a substantially lower density than their neighbors.

The number of neighbors considered, (parameter n_neighbors) is typically chosen 1) greater than the minimum number of objects a cluster has to contain, so that other objects can be local outliers relative to this cluster, and 2) smaller than the maximum number of close by objects that can potentially be local outliers. In practice, such informations are generally not available, and taking n_neighbors=20 appears to work well in general.


# Conclusion
- This is a great dataset to learn about binary classification problem with unbalanced data.
- As the features are disguised, feature selection cannot be assisted based on the domain knowledge of the topic. Statistical tests hold the complete importance to select features for modeling.
- Due to the use of SMOTE analysis for balancing the data, the models trained on this synthetic data cannot be evaluated using accuracy. Hence, we resort to Cross Validation Score and ROC-AUC Score for model evaluation.
- Several machine learning algorithms and techniques are commonly used for credit card fraud detection, including logistic regression, support vector machines (SVM), k-nearest neighbors (KNN), decision trees, random forests, isolation forests, and local outlier factor (LOF).
- Each algorithm has its strengths and weaknesses, and the choice depends on factors such as dataset characteristics, interpretability, computational efficiency, and performance metrics.
- Evaluation metrics play a crucial role in assessing the performance of fraud detection models. Common metrics include CV Score, F1-score, ROC AUC score, and confusion matrix. These metrics provide insights into the model's ability to correctly classify normal and fraudulent transactions, minimize false positives and false negatives, and overall effectiveness in fraud detection.

# Future Directions
The research highlights the importance of ongoing research and innovation in the field of credit card fraud detection. Future directions may include exploring advanced machine learning techniques, such as deep learning and reinforcement learning, integrating behavioral analytics and biometric authentication, leveraging blockchain technology for secure transactions, and enhancing collaboration between academia, industry, and regulatory bodies to address emerging challenges and threats in fraud detection.

# # References :

- https://www.chargebackgurus.com/blog/credit-card-fraud-detection
- https://www.cnbc.com/select/what-is-a-credit-card/
- https://www.bajajfinserv.in/credit-card-fraud-in-india
- https://www.fortunebusinessinsights.com/industry-reports/fraud-detection-and-prevention-market-100231
