Titanic Survival Analysis & Feature Engineering (EDA Project)

#Project Overview
This project performs Exploratory Data Analysis (EDA) and feature engineering on the famous Titanic dataset to understand the factors that influenced passenger survival.

The workflow includes:
Data cleaning
Missing value handling
Feature creation
Categorical encoding
Statistical analysis
Data visualization
Insight generation

#Objective
To analyze Titanic passenger data and identify key factors affecting survival such as:

Passenger class
Gender
Age
Family size
Embarkation point
Titles (Mr, Mrs, etc.)

Dataset Description
The dataset contains the following features:

Column	Description
PassengerId	Unique ID of passenger
Survived	Survival (0 = No, 1 = Yes)
Pclass	Ticket class (1st, 2nd, 3rd)
Name	Passenger name
Sex	Gender
Age	Age of passenger
SibSp	Siblings/Spouses aboard
Parch	Parents/Children aboard
Ticket	Ticket number
Fare	Ticket fare
Cabin	Cabin number
Embarked	Port of Embarkation

 Data Cleaning & Feature Engineering
🔸 Handling Missing Values
Age → filled using median age grouped by Title + Pclass
Embarked → filled with mode
Fare → filled with median
Cabin → replaced with "Unknown"

🔸 Feature Extraction
1. Title Extraction

Titles extracted from names:

Mr, Mrs, Miss, Master, Rare

Rare titles grouped:

Lady, Countess, Capt, Col, Don, Dr, Major, Rev, Sir, Jonkheer, Dona
2. Family Features
FamilySize = SibSp + Parch + 1
IsAlone = 1 if FamilySize == 1 else 0
3. Age Grouping
Child (0–12)
Teen (12–18)
Young Adult (18–30)
Adult (30–50)
Senior (50+)

🔸 Encoding
Sex → male: 0, female: 1
Embarked → S: 0, C: 1, Q: 2
📊 Exploratory Data Analysis (EDA)
🔹 Survival Analysis
Higher survival in 1st class passengers
Females had significantly higher survival rate
Children had better survival chances
Passengers traveling alone had lower survival rate

🔹 Key Insights
📌 Survival by Class
1st class: 63% survival
2nd class: 47% survival
3rd class: 24% survival
📌 Survival by Gender
Female survival rate significantly higher than males
📌 Survival by Embarkation
C (Cherbourg) had highest survival rate

🔹 Family Impact
Families had higher survival rate (50%+)
Singles had lower survival rate (~30%)

🔹 Age Insights
Children had highest survival probability (~57%)
Young adults had lowest survival rate (~29%)

🔹 Title Insights
Mrs → highest survival (~79%)
Miss → high survival (~70%)
Mr → lowest survival (~15%)

📈 Visualizations Used
Bar plots (Survival by Class, Sex)
Histogram (Age distribution)
Pie chart (Passenger class distribution)
Box plot (Fare distribution)
Violin plot (Age vs Class vs Survival)
Correlation heatmap

📊 Final Summary
This analysis shows that survival was strongly influenced by:
✔ Gender
✔ Passenger class
✔ Age group
✔ Family size
✔ Social status (Title)

🛠️ Technologies Used
Python 
Pandas
NumPy
Matplotlib
Seaborn

Conclusion

The Titanic dataset demonstrates how social and economic factors heavily influenced survival outcomes. This project provides a strong foundation for:
Data preprocessing
Feature engineering
Exploratory data analysis
Beginner machine learning workflows
