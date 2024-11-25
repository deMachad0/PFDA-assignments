# PFDA-assignments

## Task 2 - Create a jupyter notebook called assignment2-weather.ipynb that has a nice plot of the temperature over time ( "dryBulbTemperature_Celsius" ). 

### Explanation
1. File Path and Variables:
Setting up the file path and why variables like total_dryBulbTemperature_Celsius and count are needed.
2. Reading Data:
csv.DictReader uses the header row to identify columns, and check for the column "dryBulbTemperature_Celsius" before processing.
3. Calculating Average:
Calculate the average temperature by adding up all valid temperatures and dividing by the count.
4. Visualizing Data:
Create a graph, plot the individual temperature readings, and highlight the average temperature with a red dashed line.
5. Error Handling:
If the file is missing (prints an error message).

---

## Task 3 - Create a notebook called assignment03-pie.ipynb. The note book should have a nice pie chart of peoples email domains in the csv file at the url
## *https://drive.google.com/uc?id=1AWPf-pJodJKeHsARQK_RHiNsE8fjPCVK&export=download
## This csv file has 1000 people. You may download the data or link to it.

### Explanation
1. Dataset Loading:
Data is fetched from an online CSV file and inspected using df.head().
2. Date Conversion:
Converts the date strings to datetime objects for easier manipulation.
3. Age Calculation:
Calculates each person's age by comparing their birthdate to the current date and adjusts for birthdays that haven’t happened yet.
4. Age Grouping:
Bins ages into predefined ranges using pd.cut() and assigns labels for these groups.
5. Visualization:
Uses a pie chart to display the distribution of employees across age groups, with percentage labels for clarity.

---

## Task 5 - Write a program (or notebook) called assignment_5_risk (.py or .ipynb). The program should simulates 1000 individual battle rounds in Risk (3 attacker vs 2 defender) and plots the result.
## One battle round is one shake of the attacker and defender dice.
## Rules of Risk:
## In Risk one army fights another. (using 6 sided dice)
## In each battle round, the attacker can put forward up to three of ## their troops (3 dice).
## The defender can use up to two of their defending troops (2 dice).

### Explanation 
1. Simulating Dice Rolls:
The attacker rolls three dice, and the defender rolls two dice. Random rolls are generated using np.random.randint.
2. Finding the Winners:
The maximum value of each set of dice rolls is compared. If the attacker's max roll is higher, they win; otherwise, the defender wins.
3. Tracking Results:
The total wins for the attacker and defender are counted in attacker_wins and defender_wins.
4. Calculating Percentages:
The win percentages are calculated as (wins / total battles) * 100.
5. Visualizing Results:
Pie Chart: Shows the percentage of wins for each side.
Bar Chart: Displays the absolute number of wins for both sides.

---

## Task 6 - Create a python file or notebook called assignment_6_Weather (.py or .ipynb)
## Get the data from this link.
## *https://cli.fusio.net/cli/climate_data/webdata/hly4935.csv
## Plot:
## The temperature
## The mean temperature each day
## The mean temperature for each month

### Explanation
1. Load the dataset: 
Loads the dataset from the given URL. Skips the first 23 rows, assuming they contain metadata or headers unrelated to the main data.
2. Data conversion and processing:
Converts the date column from a string to a proper datetime format and removes time details (hour and minute) using normalize().
3. Temperature analysis: 
Groups the data by year ('YE') and calculates the average temperature for each year, Creates a line plot showing the yearly average temperature over time.
Groups the data by month ('ME') and calculates the average temperature for each month.
4. Wind speed analysis:
Converts the wdsp (wind speed) column to numeric format. Non-numeric values are replaced with NaN. Treats zeros in the wdsp column as missing data by replacing them with NaN.
Calculates the average wind speed for each year.Calculates the average wind speed for each month.
5. Visualizations:
Yearly Trends: Line plots of yearly averages show long-term trends for temperature and wind speed.
Monthly Trends: Line plots of monthly averages highlight seasonal patterns.

---
