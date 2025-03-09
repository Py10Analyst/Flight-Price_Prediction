# Flight-Price_Prediction:Flight-Price_Prediction@Kaggle_Dataset: EDA+Feature_Engineering

Objective:
The goal of this project is to analyze flight pricing data using Exploratory Data Analysis (EDA) and Feature Engineering (FE) to understand the factors affecting flight prices and prepare the dataset for predictive modeling.

Key Features:
1.	Airline – The airline operating the flight (Categorical).
2.	Flight – Flight code (Categorical).
3.	Source City – The departure city (Categorical).
4.	Departure Time – The time slot when the flight departs (Derived Feature, Categorical).
5.	Stops – The number of stops during the journey (Categorical).
6.	Arrival Time – The time slot when the flight arrives (Derived Feature, Categorical).
7.	Destination City – The arrival city (Categorical).
8.	Class – Type of seat (Economy/Business, Categorical).
9.	Duration – Flight duration in hours (Continuous).
10.	Days Left – Number of days left before departure (Derived Feature, Continuous).
11.	Price – The ticket price (Target Variable, Continuous).

Steps Followed in the Project
1.) Data Loading & Initial Exploration
•	Loaded the dataset using pandas (pd.read_excel('flight_price.xlsx')).
•	Checked the first few rows (df.head()) and basic summary (df.info(), df.describe()).
•	Verified data types and checked for missing values.
2.) Exploratory Data Analysis (EDA)
•	Univariate Analysis (Visualizing single features):
o	Used seaborn (sns) and matplotlib (plt) for plotting distributions.
o	Histograms, bar charts, and count plots were used to analyze categorical and numerical variables.
•	Bivariate Analysis (Relationship between features):
o	Boxplots and scatterplots were used to analyze Price vs. different features (e.g., sns.boxplot(x='Airline', y='Price', data=df)).
o	Correlation matrix was plotted using sns.heatmap(df.corr(), annot=True) to see which features impact the price most.
3.) Feature Engineering (FE)
•	Created New Features:
o	"Days Left" – Difference between booking date and departure date.
o	Categorized "Departure Time" and "Arrival Time" – Grouped into bins (Morning, Afternoon, Evening, Night).
•	Handled Missing Data:
o	Used .fillna() for missing values or dropped rows if necessary.
•	Encoded Categorical Features:
o	Used One-Hot Encoding for categorical variables to convert them into numerical format.

Conclusion:
1.	 Loaded and explored dataset.
2.	Performed data visualization (EDA)
3.	 Created new features ("Days Left", "Departure Time Category")
4.	Encoded categorical features.
5.	Handled outliers using IQR method.
6.	Saved cleaned dataset for further modeling.
   
Potential Next Steps:
#Feature Selection – Remove less important features to improve model performance.
#Outlier Detection & Removal – Use boxplots and IQR method to remove extreme values.
#Machine Learning Models – Train models like Linear Regression, Decision Trees, or Random Forest for flight price prediction.


