# Customer Segmentation with K-modes
Electric Vehicle Customer Segmentation

# 1. Business Framing & Project overview

## Background
Indonesia’s transportation sector, including automotive industry, has been the highest final energy consumer, contribute 27% of total energy use & become primary source of CO2 emissions in the road transportation sector.
As carbon emissions and reliance on fossil energy have become important concerns in Indonesia, developing electric vehicles is considered a possible solution due to their energy efficiency.
The project's key contribution is its approach to segmenting the battery electric vehicle market using different groups of consumer profiles.

## Dataset source information
Dataset source from my own personal survey for academic purpose.

## Objective
This project is try to answer below business question:
1.   What is the segmentation and characteristic of Indonesian battery electric vehicles?
2.   What is the most suitable battery electric vehicle basic product concept for each segmented market?


# 2. Data understanding

## Data Preparation
Packages: Pandas, Numpy, Matplotlib, Seaborn, and Sklearn.

## Data Information
Feature information:
*   `Respondent ID`: Index of each Respondent.
*   `Gender`: Gender of each respondent, there are Male & Female.
*   `Age Range (Years)`: Age range of respondent, Divided into 3 category: Gen Z (18-24), Millenials (25-40), Boomers (above 40)
*   `Domicile`: City or Region of each respondent in Indonesia area. There are : West Java, Jakarta surround area, East Indonesia, Sumatera, Borneo & Center & East Java
*   `Marital Status`: Status of marriage, Married or Unmarried.
*   `Education`: Education level from each respondent divided into 3 category: High School, Bachelor & master/Phd.
*   `Occupation`: Profession of each respondent, There are: Private Employee, Student, Self-employed, Government Employees, Housewife, Teacher/Lecturer, Retired & Others.
*   `Spending in a year`: Number of spending in a year indicates purchases power, there are: <200 M IDR, 200-250 M IDR, 250-300 M IDR, 300-350 M IDR & above 350 M IDR.
*   `Vehicle Purchase Price`: Purchase price range of Electric Vehicle that would be pay by respondent, there are 300-400 M IDR, 400-500 M IDR & above 500 M IDR.
*   `Vehicle Model`: Type of favorable electric car model, There are: City Car, MPV, SUV & Sedan 
*   `Battery Charging Time`: Total time of charging Electric car battery for 100 Km. There 3 hours, 5 hours & 8 hours.
*  `Driving Range`: Total maximum lentgh of driving in Km, divided into 250 Km, 300 Km, 350 Km.

## Data Info
1. Data contains 12 columns with 422 rows.
2. Several columns have missing values, will handle later.
3. All dtypes is categorical.


# 3. Exploratory Data Analysis

## Spending per year with Vehicle Purchase relation
![image](https://user-images.githubusercontent.com/114860846/194760875-72ad85a9-20f2-4e55-a5f4-74fa0ec548f1.png)

Respondent with Spending < 200 M IDR up to 300 M IDR consider to buy electric vehicle with price 300-400 M IDR. While Respondent with Spending 300 - above 350 M IDR consider Electric Vehicle with price above 500 M IDR.

## Age Range with Vehicle Model relation
![image](https://user-images.githubusercontent.com/114860846/194760923-39cdac0c-bddd-4902-b188-178eee3904cf.png)

Millenials favorable MPV, City car, Gen-z love City car & Babyboomers love MPV & City Car.


# 4. Clustering model (K-modes)

1. K-Modes Intialization
2. Choose k (number of cluster) by elbow method
3. Combining predicted cluster with Original dataframe


# 5. Cluster/Segment Identification
![image](https://user-images.githubusercontent.com/114860846/194761327-7ac80faf-8093-4890-9bd5-11727bf8d04f.png)

## First Cluster - "Price Sensitive"
*   Cluster #1 is the biggest segment with 280 members or 
67% of total participants. This segment is a price-sensitive 
group that prioritizes purchasing price when choosing 
battery-electric vehicles and considers City Car vehicle model with 3 hrs charging time & 350 Km Driving Range.
*   This Cluster dominated by Female, Millenials (25-40 years old). Mostly live in West Java. Most of them are married with Bachelor as the last education & Private employee as their profession. They spend less than 200 million rupiahs/year.

## Second Cluster - "Value Seeker"
*   Cluster #2 is second biggest segment with 83 members or 20% of total participants. This segment is a Value Seeker group that prioritizes purchasing price when choosing electric vehicles but still looking for affordable value in class and considers MPV vehicle model with 3 hrs charging time & 350 Km Driving Range.
*   This Cluster dominated by Male, gen-Z (18-24 years old). Mostly live in Jakarta surround area. Most of them are single with Bachelor as the last education & Student as their profession. They spend less than 200 million rupiahs/year.

## Third Cluster - "Premium"
*   Cluster #3 is the last segment with 54 members or 13% of total participants. This segment is a Premium group that looking for best value in class when choosing electric vehicles,  they considers MPV vehicle model with 5 hrs charging time & 350 Km Driving Range.
*   This Cluster dominated by Male, Milenialls (25-40 years old). Mostly live in Jakarta surround area. Most of them are Married with Bachelor as the last education & Private employee as their profession. They spend between 200-250 million rupiahs/year.


# 6. Conclusion & Recommendation

## Conclusion
There are 3 cluster/segment of Electric vehicle indetified by this project:
*   Cluster #1 is the biggest segment with 280 members or 67% of total participants. This segment is a **Price-Sensitive group** that prioritizes purchasing price when choosing battery-electric vehicles. This Cluster dominated by Female, Millenials (25-40 years old). Mostly live in West Java. Most of them are married with Bachelor as the last education & Private employee as their profession. They spend less than 200 million rupiahs/year.  
*   Cluster #2 is second biggest segment with 83 members or 20% of total participants. This segment is a **Value Seeker group** that prioritizes purchasing price when choosing electric vehicles but still looking for affordable value in class. This Cluster dominated by Male, gen-Z (18-24 years old). Mostly live in Jakarta surround area. Most of them are single with Bachelor as the last education & Student as their profession. They spend less than 200 million rupiahs/year.
*   Cluster #3 is the last segment with 54 members or 13% of total participants. This segment is a **Premium group** that looking for best value in class when choosing electric vehicles.This Cluster dominated by Male, Milenialls (25-40 years old). Mostly live in Jakarta surround area. Most of them are Married with Bachelor as the last education & Private employee as their profession. They spend between 200-250 million rupiahs/year.

## Recommendation
There are 3 Basic Product Attribute/ Product Concept that suitable for each cluster/segment of Electric vehicle:
*   Cluster #1 **Price-Sensitive** --> City Car vehicle model with 3 hrs charging time & 350 Km Driving Range.
*   Cluster #2 **Value Seeker** --> MPV vehicle model with 3 hrs charging time & 350 Km Driving Range. 
*   Cluster #3 **Premium** --> MPV vehicle model with 5 hrs charging time & 350 Km Driving Range.

