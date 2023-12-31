**EXPERMENTATION OF THE ONLINE PAYMENT FRAUDS DETECTION** 

**Description**

There has been a rapid rise in online transactions across many domains since the expansion of modern technology and global communication. Many companies including taxation, e-commerce, healthcare system, management, and banking now have an online presence where transactions can be done easily. Despite the advantages this brings to the lives of the people, customers still face a lot of problems due to financial fraud. The advancement of digital services further caused a surge in financial crime.
In this work, data analytics and machine learning techniques in financial transaction fraud detection was implemented. Efficient procedures and models that make use of data analysis methodologies to identify and mitigate fraudulent financial transaction activity was also developed
Goal
The study aims to use analytics, and machine learning algorithms such as Decision Tree (DT), Random Forest (RF), Naive Bayes (NB) and Logistic Regression (LR) to train,test, find trends and anomalies that point to fraudulent conduct, helping financial institutions, companies, and regulatory authorities identify and reduce financial transaction fraud.

**Dataset**

The Online payments big dataset was contributed in kaggle by Rupak Bob Roy. It captures different types of transaction routes, each of which can be used to carry out fraud activity (CASH OUT, PAYMENT, CASH IN, TRANSFER, and DEBIT). The dataset also consists of other relevant features like hours of transactions, the account balance of the transaction initiator and recipient before and after the transaction, and many more features that are informative for analysis and fraud detection models. Moreover, The dataset is made up of 6,362,620 rows and 11 columns. Fraudulent transactions are recorded in 8213 rows which is 0.00046% of the dataset and 6,354,407 are non-fraudulent which comprises 0.99954% of the dataset. The distribution ratio of the transactions indicates class imbalance.

**Objectives**

**Data Preprocessing**

Before conducting further analysis, the online payment transaction dataset will be subjected to preprocessing. Data Preprocessing encompasses different processes like data cleaning, data transformation, and preparing raw data for proper modeling.
To start with, the data quality and tidiness will be observed. Afterward, misspelled words, null and missing values will be checked for, if anyone is found, it will be dropped, corrected, and replaced by extrapolation where necessary. The data type of each feature will be observed and corrected for better data representation. Moreover, Data normalization and scaling will be carried out to evaluate its effect of the model. 

**Data visualization**
In this section, data visualization will be implemented to showcase various insights and statistics from the dataset.  Visualizations of different types will be grouped into segments. Univariate, Bivariate, and Multivariate exploration will demonstrate different plots and charts like doughnuts pie charts, bar charts, distribution plots, box plot, line plots, correlation maps, and histograms. This will serve as a virtual representation of the relationship and patterns between the Features. Python libraries for visualization will include: Matplotlib, plotly, Seaborn, and pandas.

**Feature Engineering**
In an attempt to feed the model with the right representation of the underlying data for easy learning, Feature engineering will be performed.  New features will be created from the existing features in the dataset. Some of these new features may include hour of the day, day of the week, amount to oldbalanceOrg, amount to oldbalanceDest, originator transaction freq, recipient_transaction_freq, originator balance change, and destination balance change. These features will allow the model to capture the nonlinear relationship between variables, hence, the model will be able to learn more patterns in the data.

**Feature Selection**
Given the number of variables in the dataset after feature engineering, it's imperative to select those that best predict the dependent variable. These sections help to check the effect of feature selection on the models’ performance. Furthermore, answers the research question of which feature selection has the most impact on the model performance.
The feature selection techniques including SelectKbest, Boruta feature selection, and recursive feature elimination were used respectively to select the best subset of features in order of importance. The subsets of the dataset obtained were used on the models.

**Data sampling**

The Online payment dataset contains highly imbalanced samples which constitute 0.00046% of fraudulent cases and 0.99954% of non fradulent cases. This problem leads to bias during training with the model giving more focus on the majority class. To deal with this, the Synthetic Minority Oversampling Technique (SMOTE) oversampling technique will be implemented.  The SMOTE will help to generate synthetic samples which are added to the original dataset to increase the number of samples in the minority class. This will result in a balanced distribution between the classes. Therefore, the model will be able to train well without bias. 
**Model Building:** The datasets were trained on five ML models which are logistic regression, decision tree, random forest, naive Bayes, and support vector machine. This was done without prior application of the feature selection technique to check the performance of the models. The results in figure 4.19 show that Random Forest performed much better with 99.98% accuracy and 0.98 AUC while the naive bayes have the least performance with 97.17% accuracy and 0.83 AUC.

 **Model Evaluation:** Rigorously evaluate model performance using appropriate metrics. Through meticulous evaluation, select the most effective and precise predictive model.
**Interpretability:** Unearth the influential factors that shape house prices. Interpret the model results to gain valuable insights into the dynamics of the real estate market.
**Business Impact:** Translate model insights into actionable strategies that can transform Wazobia Real Estate's pricing tactics and enhance their competitive edge.

**Installation**
-	Run the Google Collaboratory

**Findings and Limitations**

This report uses data analytics and machine learning approaches in detecting financial fraud.  Several models such as Logistic regression (LR), Decision tree (DT), Random Forest (RF), Naive Bayes (NB), Support vector machine (SVM), and techniques like feature selection were experimented with to find the best methods that effectively detect fraudulent transactions. The result shows that Random Forest outperformed other models used in the experiment. The performance of Random Forest is evident in many literatures (Varmedja et al, 2019, Manjeevan et al., 2021).
There are many literatures that emphasize the importance of feature selection and data sampling in improving model performance. On the contrary, some literature also reported that the application of feature selection has negligible or no effect on the model performance. This shows that there is no "best method" that is fit for all problem settings. This effect on the model performance depends on the dataset and the feature selection methods used.
Experimental findings from this study show that the implementation of feature selection methods has no significant impact on the baseline model's performance. The application of methods like Boruta feature selection and SelectKbest with Random Forest have the same superior accuracy of 98% as the baseline model performance without prior application of feature selection technique and the same Naive Bayes model performance of 97.17% accuracy as the least while the recursive feature elimination method decreases the baseline model performance of the decision tree, naive Bayes, and random Forest. This study confirms the outcome of Jiarpakdee et al in the literature. Nevertheless, the implementation of feature selection is evident in many literatures to increase the model performance. Using the right feature selection technique can impact the model's performance (Hasan & Bao 2021, Reddy et al. 2019, Sharma et al., (2021). Moreover, of all the feature selection methods experimented with, the impact of Boruta feature selection on the overall model performance overweighed other techniques. 
