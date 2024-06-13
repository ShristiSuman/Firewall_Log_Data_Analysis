# Predictive Analysis of Firewall Log Data for Network Security

## Abstract
The analysis of firewall log data is crucial for network security, allowing the monitoring and classification of network traffic patterns. This study develops predictive models to classify incoming traffic into four categories: "Allow," "Drop," "Deny," and "Reset-both." Using comprehensive internet traffic records from a university firewall, various machine learning and deep learning algorithms are applied, including Random Forest, Support Vector Machines, Deep Neural Networks, Logistic Regression, and K-Nearest Neighbors. Our findings show that the Random Forest model is the most effective in accurately classifying the multi-class firewall log data, enhancing the detection and mitigation of potential security threats and providing network administrators with a powerful tool for proactive threat assessment.

## Introduction
Internet firewalls are essential for protecting networks from unauthorized access and cyber threats. This project aims to automate the classification and analysis of firewall log data using machine learning, addressing the limitations of manual rule configuration. By leveraging historical data from firewall logs, machine learning algorithms can identify patterns and predict security threats, improving accuracy in threat detection and enabling faster decision-making.

## Data Description
The dataset used in this study is sourced from the UCI Machine Learning Repository. It includes 12 features: source port, destination port, NAT source port, NAT destination port, action, bytes, bytes sent, bytes received, packets, elapsed time (in seconds), packets sent, and packets received. The "Action" attribute serves as the class identifier.

## Exploratory Data Analysis (EDA)
Visual explorations are performed using histograms, count plots, and crosstabs to understand distributions and relationships in the data. Insights regarding port usage, action distributions, and correlations between features are drawn.

## Methodology
### Data Pre-processing
Data pre-processing involved removing redundant records, handling missing values, balancing the dataset using resampling techniques, normalizing the data, and applying one-hot encoding to categorical variables.

### Feature Selection
Feature selection was performed using Chi-Square tests, Forward Feature Selection, Backward Elimination, Recursive Feature Elimination with Cross-Validation (RFECV), and Lasso Regularization. The top five features selected were: Source Port, Destination Port, NAT Source Port, NAT Destination Port, and Elapsed Time (sec).

### Implemented Models
The following supervised models were implemented:

- Random Forest
- Multinomial Logistic Regression
- Support Vector Machines (SVM) with RBF kernel
- K-Nearest Neighbors (KNN)
- Deep Neural Networks (DNN)

### Hyperparameter Tuning
Hyperparameters were tuned using RandomizedSearchCV and GridSearchCV from Scikit-Learn. 

## Evaluation Metrics
The performance of the models was evaluated using accuracy, precision, recall, and F1-score.

## Results/Findings
The Random Forest model demonstrated the highest accuracy (99.6%) and F1-score (0.996), followed by KNN, SVM, Logistic Regression, and DNN. The results suggest that Random Forest and KNN are the most effective algorithms for classifying internet firewall data.

## Conclusion and Discussion
The study highlights the efficacy of the Random Forest classifier in accurately classifying internet firewall data. The most significant predictors for classifying network traffic were Source Port, Destination Port, NAT Source Port, NAT Destination Port, and Elapsed Time. The Random Forest model's minimal misclassifications and high scores in key metrics underline its reliability and robustness.
