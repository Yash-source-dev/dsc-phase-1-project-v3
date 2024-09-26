### Aviation Accident Data Analysis Project
![pexels-chevanon-333525](https://github.com/user-attachments/assets/b9593b89-18da-4231-a419-1d75b07b01f2)

## Project Overview
This project focuses on analyzing aviation accident data to identify the safest aircraft models and related risk factors. The objective is to help our company make informed decisions about purchasing aircraft based on accident risk, model reliability, and other key factors. The data is drawn from the Aviation Accident Database & Synopses (up to 2023), and the project leverages tools like Python for data analysis and Tableau for visualizing results.

## Business Understanding
The analysis is driven by the following core business questions:
Which aircraft models are associated with the highest number of accidents?
Which locations have experienced the highest frequency of aviation accidents?
How does injury severity vary by aircraft model?
What is the relationship between aircraft model, category, and damage incurred?
Which aircraft models have a high incidence of accidents based on their manufacturing locations?
What is the most reliable engine type in terms of accident rates?
Which aircraft models incur the most accidents based on their purpose of flight (e.g., commercial, private)?
Is there a correlation between weather conditions and the occurrence of accidents? Additionally, is there a correlation between weather and accident locations?
How many accidents occur in each phase of flight (e.g., takeoff, landing, cruising)?
Are there specific conditions (e.g., weather, aircraft type) that correlate with accidents in particular flight phases?
The primary goal is to identify aircraft models and conditions that lead to higher accident rates, enabling safer aircraft purchase decisions.

## Data Description
The dataset includes aviation accidents and incidents up to 2023, with the following key columns:
Event.Id, Accident.Number, Event.Date, Location, Country, Injury.Severity, Aircraft.Damage, Aircraft.Category, Make, Model, Engine.Type, Purpose.of.Flight, Weather.Condition, Broad.Phase.of.Flight, Total.Fatal.Injuries, Total.Serious.Injuries, Total.Minor.Injuries, Total.Uninjured.
Data Cleaning Process
The raw data required extensive preprocessing, including:
Duplicate Removal: Removed duplicate entries for accidents.
Missing Data Handling: Used mean, median, and mode imputation to fill missing values.
Unnecessary Columns Dropped: Columns not relevant to the analysis were removed to streamline the dataset.
The final cleaned dataset allowed for focused analysis on aircraft models, locations, injury severity, and other critical factors.

## Data Analysis
The analysis was conducted to address each business question. Key steps include:
Grouping Data: Aggregated data by aircraft models, locations, weather conditions, etc.
Correlation Analysis: Analyzed relationships between accident rates and various factors like weather conditions and flight phases.
Injury Severity Analysis: Examined how injury severities (fatal, serious, minor) vary by aircraft model.
Filtering and Ranking: Ranked aircraft models by accident frequency and filtered for insights on specific conditions (weather, location, etc.).
Example of Key Analysis:
Injury Severity by Aircraft Model: Used Tableau to create bar charts and box plots visualizing how injury severity differs across aircraft models, with models like X showing higher rates of serious and fatal injuries.
Correlation Between Weather and Accidents: Conducted correlation analysis in Tableau to show how weather conditions (e.g., rain, fog) significantly impact accident frequency, especially during critical flight phases like takeoff and landing.

## Aircraft model that causes alot of accidents
![image](https://github.com/user-attachments/assets/ec2f4042-5e6d-41fd-a510-8c4a870b1062)

## Aircraft model that causes few accidents
![image](https://github.com/user-attachments/assets/43a5aead-6510-4752-8634-c6f54f2ac860)

## location tht has been engaged with alot of accidents?
![image](https://github.com/user-attachments/assets/39587dd8-963e-482a-8146-9f450f1c7b2b)

##location with least accidents?
![image](https://github.com/user-attachments/assets/ea8fee6a-7437-42b6-bf40-b77a88caac1e)

## 3.What are in these locations that cause a lot of accidents?
.can these two be the reason['Weather.Condition', 'Broad.phase.of.flight',]
.and what percantage do they contribute?

                  Location Weather.Condition  Accidents_By_Weather  \
0         (N) SKWENTNA, AK               VMC                     1   
1                        ,               VMC                     2   
2                     , AO               VMC                     2   
3               0WASSO, OK               VMC                     1   
4      1 1/2 MI.N. MAY, KS               IMC                     1   
...                    ...               ...                   ...   
25167           Zillah, WA               VMC                     1   
25168       Zionsville, IN               VMC                     2   
25169     Zurich, Eswatini               IMC                     1   
25170          Zwingle, IA               VMC                     1   
25171           helena, MT               VMC                     1   

       Total_Accidents  Weather_Percentage  
0                    1               100.0  
1                    2               100.0  
2                    2               100.0  
3                    1               100.0  
4                    1               100.0  
...                ...                 ...  
25167                1               100.0  
25168                2               100.0  
25169                1               100.0  
25170                1               100.0  
25171                1               100.0 


### according to my research
### vmc=is good weather
### IMC=bad weather
### lets find out the weather that occured much during accidents

Weather.Condition	Accident_Count
0	IMC	5116
1	UNK	634
2	Unk	48
3	VMC	70190

## Plotting the graph to show whhich weather condition occured most 

![image](https://github.com/user-attachments/assets/0cb7cac2-0f7e-4cc2-aa26-f2201d494c85)

### from our analysis VMC has occured alot which means the weather conditions were good.Therefore,weather conditions is a least factor tht affects the accidents

### Correlation between Weather Condition and Accident Count: 0.7346408009582759

## ### 4 which aircafts incurred alot of accidents depending on Purpose.of.flight?
### How many accidents occur in each phase of flight?

  Broad.phase.of.flight  Accident_Count
12               unknown           17194
5                Landing           14897
9                Takeoff           12094
2                 Cruise            9698
6            Maneuvering            7989
0               Approach            6220
1                  Climb            1849
10                  Taxi            1736
3                Descent            1676
4              Go-around            1336
8               Standing             677
11               Unknown             512
7                  Other             110

## 5 can these two be the reason['Weather.Condition', 'Broad.phase.of.flight',]?
Weather.Condition       IMC  UNK  Unk    VMC
Broad.phase.of.flight                       
Approach                915   32    0   5273
Climb                   254   20    0   1575
Cruise                 1548  193    0   7957
Descent                 183   17    0   1476
Go-around               149    3    0   1184
Landing                 372   48    0  14477
Maneuvering             435   62    0   7492
Other                     3    2    0    105
Standing                 16   15    0    646
Takeoff                 422   36    0  11636
Taxi                     49    9    0   1678
Unknown                  54   79    0    379
unknown                 716  118   48  16312

![image](https://github.com/user-attachments/assets/e0c07b32-cbcf-4a84-accc-379b469b8d66)


## injury severity depending on the aircraft model?
## Injury Severity by Top 30 Aircraft Models
![image](https://github.com/user-attachments/assets/59f01f26-2f42-4f0e-81f5-14a02c5a005b)
## Injury Severity by Least 30 Aircraft Models
![image](https://github.com/user-attachments/assets/bb5e3568-f99a-46a9-89fd-e2f522b6548a)
from the 2 bar graphs my advice is for u to choose an aircraft model(top 30 aircraft models with the least number of injuries.) which will be safer incase of an accident.

## ## 7.the best engine type in an aircraft?
Top 30 Engine Types by Number of Accidents
![image](https://github.com/user-attachments/assets/f72cfb28-83be-4c0e-b030-bd0d94020b6c)
![image](https://github.com/user-attachments/assets/e7d56717-936c-417e-89d8-1aed1ced25a4)
Top 30 Engine Types by Number of Accidents
![image](https://github.com/user-attachments/assets/84d115f3-43fe-4174-8cb9-c3e76ee3ee0e)
from the two scatter plots u are able to chose the best engine_type.

## Tableau Dashboards
## Visualization and Filters
The dashboards in Tableau are designed to answer the business questions interactively.
https://public.tableau.com/app/profile/samuel.yashua7815/viz/Book1_17273347252670/Dashboard1?publish=yes
## Recommendations
Based on the analysis, the following recommendations can be made:
.Consider purchasing aircraft models with a low incidence of accidents and high reliability based on injury severity and damage data.
.Select aircraft with the most reliable engine types, as these have been shown to have lower accident rates.
. Pay attention to weather patterns and accident-prone locations when planning flights, especially during certain phases like takeoff and landing.
## Next Steps
Further Exploration: Conduct deeper analysis into aircraft categories and compare accident rates based on newer aircraft models.
Implementation of Predictive Models: Use machine learning models to predict the likelihood of accidents based on aircraft, weather, and location data.
Expansion to Other Datasets: Incorporate more global aviation data to broaden the scope of the analysis.
## Conclusion
This project provides valuable insights into aviation safety by analyzing accident data across various dimensions. The visualizations generated in Tableau allow for a clear understanding of which factors contribute to accidents, and the recommendations help guide decisions regarding aircraft purchases and risk management.
## Presentation Link
file:///C:/Users/ADMIN/Downloads/Aviation%20Accident%20Data%20Analysis.pdf





