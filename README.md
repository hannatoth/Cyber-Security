# Fraud detection in transactions


🌸 Project Overview

This project focuses on detecting fraudulent activities in financial transactions using a data-driven approach. The analysis is centered around identifying patterns and discrepancies in transaction data, particularly between flagged and non-flagged frauds.

🌸 Dataset

The dataset includes financial transactions with a particular emphasis on transfer-type transactions. Key features analyzed include original old balance, maximum and minimum balances in both flagged and non-flagged transactions.

<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>step</th>
      <th>type</th>
      <th>amount</th>
      <th>nameOrig</th>
      <th>oldbalanceOrg</th>
      <th>newbalanceOrig</th>
      <th>nameDest</th>
      <th>oldbalanceDest</th>
      <th>newbalanceDest</th>
      <th>isFraud</th>
      <th>isFlaggedFraud</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>74247</th>
      <td>10</td>
      <td>CASH_IN</td>
      <td>702363.89</td>
      <td>C194439854</td>
      <td>2255173.81</td>
      <td>2957537.70</td>
      <td>C2078011503</td>
      <td>1873190.85</td>
      <td>1342688.22</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3272373</th>
      <td>251</td>
      <td>CASH_IN</td>
      <td>104826.78</td>
      <td>C808481070</td>
      <td>0.00</td>
      <td>104826.78</td>
      <td>C1595173915</td>
      <td>272496.39</td>
      <td>167669.61</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1618592</th>
      <td>157</td>
      <td>CASH_IN</td>
      <td>203485.33</td>
      <td>C151107797</td>
      <td>290.00</td>
      <td>203775.33</td>
      <td>C1899055666</td>
      <td>0.00</td>
      <td>0.00</td>
      <td>0</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>

🌸  Highlights

The analysis highlighted that the original old balance and the movements between accounts play a crucial role in distinguishing between fraudulent and non-fraudulent transactions. Flagged frauds typically showed extreme values or inconsistencies in account balances, suggesting these features are pivotal in detecting anomalies.
The application of oversampling techniques, particularly SMOTE, proved essential in addressing the class imbalance issue common in fraud detection datasets. By synthesizing new samples, we enhanced the predictive accuracy of our models, allowing for better generalization when detecting fraud in less represented transaction types.


🌸 Techniques Used  

Data cleaning and preprocessing
- Handling Missing Values: Analyzing and imputing missing data in the dataset to ensure the integrity of the analysis.
- Feature Selection: Identifying and selecting the most relevant features that contribute to detecting fraudulent activities based on statistical measures and domain knowledge.
- Data Transformation: Normalizing or scaling the data to prepare for analysis, which helps in enhancing model performance by treating all features equally.
  
Exploratory data analysis   
- Statistical Summary: Calculating summary statistics to get an overview of the data, such as mean, median, mode, and standard deviations for each feature.
- Visualization: Using plots such as histograms, box plots, and scatter plots to visualize distributions and relationships between variables. This helps in identifying patterns, anomalies, or irregularities in the data.
- Correlation Analysis: Examining the relationships between different variables to understand how they influence each other, which can be pivotal in predicting fraudulent transactions.   

Imbalance handling through oversampling   
- Oversampling Minority Class: Implementing techniques like SMOTE (Synthetic Minority Over-sampling Technique) to artificially increase the number of examples in the minority class (in this case, fraudulent transactions) to balance the dataset.
- Analyzing Impact: Assessing how oversampling influences model performance and decision-making processes in predicting fraud.

Model development and evaluation  
- Model Selection: Choosing appropriate machine learning models (e.g., logistic regression, decision trees, random forests) based on the nature of the data and the problem.
- Cross-Validation: Using techniques such as k-fold cross-validation to validate the stability and reliability of the model performance across different subsets of the dataset.
- Performance Metrics: Evaluating model effectiveness using metrics such as accuracy, precision, recall, F1-score, and ROC-AUC to determine how well the model identifies fraudulent transactions.

