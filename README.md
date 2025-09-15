# 🚢 **Titanic Dataset Analysis – Project Report**

# 🔎 **Project Overview**

The Titanic dataset analysis project aims to explore passenger data from the RMS Titanic and identify key factors that influenced survival during the disaster of 1912.
This project combines data cleaning, visualization, and data modeling (DAX in Power BI) to extract insights and build an interactive dashboard.

**Objectives:**

* Understand passenger demographics and travel details.

* Analyze how gender, age, class, and family size influenced survival chances.

* Create meaningful visualizations & KPIs in Power BI.

* Apply DAX measures for deeper insights and calculations.

#🛠 **Tools & Technologies**

* Jupyter Notebook / Python – For initial data exploration & preprocessing.

* Pandas & Numpy – Data handling and cleaning.

* Matplotlib & Seaborn – Exploratory visualizations.

* Power BI – Dashboard creation and interactive reporting.

* DAX (Data Analysis Expressions) – Calculated measures for KPIs in Power BI.

#📂 **Dataset Information**

The Titanic dataset contains passenger information with survival labels.

Key Columns:

* PassengerId – Unique ID

* Survived – (0 = No, 1 = Yes)

* Pclass – Ticket class (1, 2, 3)

* Name – Passenger name

* Sex – Male/Female

* Age – Age in years (some missing values)

* SibSp – Number of siblings/spouses aboard

* Parch – Number of parents/children aboard

* Ticket – Ticket number

* Fare – Ticket fare

* Cabin – Cabin number (many missing)

* Embarked – Port of Embarkation (C, Q, S)

#📊 **Key Visualizations**

* Some of the major visualizations used in this project include:

* Survival by Gender – Shows higher survival rate for females.

* Survival by Passenger Class (Pclass) – First class passengers survived more often.

* Age Distribution – Children had better survival chances than middle-aged men.

* Family Size vs Survival – Balanced family groups (2–4 members) had higher survival probability.

* Embarkation Port vs Survival – Variations in survival depending on port of departure.

* Fare vs Survival – Higher fares correlated with better survival chances.

#📐 **DAX Measures**

Below are some example DAX measures used:

* Total Passengers

Total Passengers = COUNTROWS(Titanic)


* Total Survivors

Total Survivors = CALCULATE(COUNTROWS(Titanic), Titanic[Survived] = 1)


* Survival Rate %

Survival Rate % = DIVIDE([Total Survivors], [Total Passengers], 0)


* Average Age of Survivors

Avg Age Survivors = CALCULATE(AVERAGE(Titanic[Age]), Titanic[Survived] = 1)


* Survival by Gender %

Survival by Gender % = 
DIVIDE(
    CALCULATE(COUNTROWS(Titanic), Titanic[Survived] = 1),
    CALCULATE(COUNTROWS(Titanic)),
    0
)


* Survival by Class %

Survival by Class % = 
DIVIDE(
    CALCULATE(COUNTROWS(Titanic), Titanic[Survived] = 1),
    CALCULATE(COUNTROWS(Titanic)),
    0
)

#✅ **Conclusion**

* Gender was the most important factor – Women had much higher survival rates than men.

* Class mattered significantly – Passengers in 1st class had the best survival chances.

* Children survived more often than adults, especially middle-aged men.

* Fare and wealth were linked to survival – higher-paying passengers had better lifeboat access.

* Family presence influenced survival – being alone reduced chances, but very large families also struggled.

