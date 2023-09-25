# Online-payment-frauds-detection

This report uses data analytics and machine learning approaches in detecting financial fraud.  Several models such as Logistic regression (LR), Decision tree (DT), Random Forest (RF), Naive Bayes (NB), Support vector machine (SVM), and techniques like feature selection were experimented with to find the best methods that effectively detect fraudulent transactions. The result shows that Random Forest outperformed other models used in the experiment. The performance of Random Forest is evident in many literatures (Varmedja et al, 2019, Manjeevan et al., 2021).
There are many literatures that emphasize the importance of feature selection and data sampling in improving model performance. On the contrary, some literature also reported that the application of feature selection has negligible or no effect on the model performance. This shows that there is no "best method" that is fit for all problem settings. This effect on the model performance depends on the dataset and the feature selection methods used.
Experimental findings from this study show that the implementation of feature selection methods has no significant impact on the baseline model's performance. The application of methods like Boruta feature selection and SelectKbest with Random Forest have the same superior accuracy of 98% as the baseline model performance without prior application of feature selection technique and the same Naive Bayes model performance of 97.17% accuracy as the least while the recursive feature elimination method decreases the baseline model performance of the decision tree, naive Bayes, and random Forest. This study confirms the outcome of Jiarpakdee et al in the literature. Nevertheless, the implementation of feature selection is evident in many literatures to increase the model performance. Using the right feature selection technique can impact the model's performance (Hasan & Bao 2021, Reddy et al. 2019, Sharma et al., (2021). Moreover, of all the feature selection methods experimented with, the impact of Boruta feature selection on the overall model performance overweighed other techniques. 
In addition, the application of synthesis minority oversampling technique (SMOTE) have no increase in the performance of the machine learning models but causes a significant decrease in Naïve Bayes model performance.
There are several technical limitations to this study. The experiments were conducted using an on-premise computer system which accompanied high computational cost and system failure sometimes. Moreover, real world dataset was not used for these experiments which question the formality of the result. Hence, the direct implementation of these findings to other may take slightly different approach like special attention to the data tidiness, quality and an advanced machine learning methods depending on the dataset. Moreover, In the case of real word data, the collection and usage of data need to comply with the privacy, security, ethics, legal and regulatory rules.



Description
Welcome to the Wazobia Real Estate Limited Predictive Modeling Hackathon! This exciting data science competition is dedicated to the accurate prediction of house prices in Nigeria. Our mission is to collaboratively develop powerful predictive models that empower Wazobia Real Estate with the insights they need to make informed pricing decisions and excel in the competitive real estate market.

Goal
The primary objective of this hackathon is to create a robust predictive model that can accurately estimate house prices in Nigeria. By harnessing the potential of the provided dataset, participants will craft sophisticated models that generate dependable price predictions for Wazobia Real Estate's diverse properties.

Objectives
Data Analysis: Delve into the dataset through comprehensive exploratory data analysis. Identify outliers, tackle missing values, and gain a deep understanding of the data's underlying characteristics.

Model Building: Employ advanced machine learning algorithms to construct predictive models. Strive for models that offer exceptional accuracy in forecasting house prices.

Model Evaluation: Rigorously evaluate model performance using appropriate metrics. Through meticulous evaluation, select the most effective and precise predictive model.

Interpretability: Unearth the influential factors that shape house prices. Interpret the model results to gain valuable insights into the dynamics of the real estate market.

Business Impact: Translate model insights into actionable strategies that can transform Wazobia Real Estate's pricing tactics and enhance their competitive edge.

Installation
To get started with the Wazobia Real Estate Predictive Modeling Hackathon, follow these installation steps:

Clone the Repository: Begin by cloning this repository to your local machine using the following command:

git clone https://github.com/FelixFrankFelix/DSN-MICROSOFT-HACKATHON.git
Navigate to the Directory: Move into the project directory:

cd DSN-MICROSOFT-HACKATHON
Create a Virtual Environment (Optional): While not mandatory, it's recommended to create a virtual environment to isolate the project dependencies. You can create a virtual environment using venv or conda. For venv, execute:

python -m venv venv
Activate the virtual environment:

On Windows:
venv\Scripts\activate
On macOS and Linux:
source venv/bin/activate
Install Dependencies: Install the required Python packages using pip:

pip install pandas numpy scikit-learn catboost seaborn matplotlib
Run the Jupyter Notebook: Launch the Jupyter Notebook to explore the provided dataset and participate in the hackathon:

jupyter notebook
Open the Notebook: In your web browser, navigate to http://localhost:8888 to access the Jupyter Notebook interface. Open the Exploratory Data Analysis.ipynb notebook to get insight about the data, then Data Preprocessing-Modelling.ipynb notebook to start your data transformation and model building journey.

That's it! You're all set to dive into the Wazobia Real Estate Predictive Modeling Hackathon. Happy coding and data exploring!

Data Description and EDA
This dataset contains valuable information on various features related to houses, including the number of bathrooms, bedrooms, parking spaces, property types, and their corresponding prices. The goal of this hackathon is to develop accurate predictive models that estimate house prices in Nigeria, providing valuable insights to Wazobia Real Estate Limited for informed decision-making and improved market competitiveness.

Data Overview
Number of Entries: 14,000
Features: Bathroom, Bedroom, Parking Space, Property Location (loc), Property Type (title), Price
Target Variable: Price
Data Analysis Highlights
In our exploratory data analysis (EDA), we delved into various aspects of the dataset to understand its characteristics and relationships. Here are some key insights:

The distribution of bathrooms, bedrooms, and parking spaces is explored, revealing trends and possible outliers.
The distribution of property prices is analyzed, highlighting skewness and the presence of outliers.
Missing values are identified in the "loc" and "title" columns, and recommendations are provided for handling them appropriately.
Correlation analysis showcases the relationships between features and the target variable (price), guiding feature selection for modeling.
Location-based and property type-based pricing trends are uncovered, offering insights for pricing strategies.
Data Access
You can access the complete dataset and participate in the hackathon on the Zindi platform: Wazobia Real Estate Hackathon Data.

Explore, analyze, and build predictive models to contribute to Wazobia Real Estate's journey towards enhanced pricing strategies and market success!

Data Preprocessing
Data Cleaning
Removed rows with missing values in 'loc' and 'title' columns.

Filled missing values in 'bedroom', 'bathroom', and 'parking_space' columns with their respective medians.

Features Engineering
Added binary indicator variables 'is_lagos' and 'is_mansion' to capture location and property type effects.

Created new features 'comfort_ind', 'size', and 'comfort_by_size' to capture property comfort and size insights.

Categorized locations based on population density into 'population_density_level'.

Encoded 'loc' column using TargetEncoder, enhancing model's understanding of location-price relationship.

Machine Learning WorkLoad
Model Building
Utilized CatBoostRegressor with RMSE as the loss function for predicting house prices.

Employed 5-fold cross-validation with shuffling using KFold to prevent overfitting.

Model Evaluation
Achieved a cross-validation RMSE score of 416,786, indicating prediction variance.

Leaderboard (LB) score of 310,010 for performance on the competition's test dataset (1st Place Score).

Features Importance
Top three important features: "loc_encoded," "title_rank," and "bedroom" (23.06%, 22.46%, 19.12%).

Significant contributions from "is_mansion" (10.31%), "size" (9.63%), "is_lagos" (4.28%), and "comfort_by_size" (3.64%).

"comfort_ind," "parking_space," and "bathroom" have relatively lower importance scores.
