# PFDA Assignments  

## Task 2 - Temperature Plot  
**File:** `assignment2-weather.ipynb`  
**Objective:** Create a Jupyter Notebook to display a plot of temperature over time using the `"dryBulbTemperature_Celsius"` column.  

### Explanation  
1. **File Path and Variables:**  
   - Set up the file path and explain the purpose of variables like `total_dryBulbTemperature_Celsius` and `count`.  

2. **Reading Data:**  
   - Use `csv.DictReader` to read the CSV file. Ensure the column `"dryBulbTemperature_Celsius"` exists before processing the data.  

3. **Calculating Average:**  
   - Compute the average temperature by summing valid temperature values and dividing by the total count of valid entries.  

4. **Visualizing Data:**  
   - Create a graph that plots individual temperature readings and overlays a red dashed line to indicate the average temperature.  

5. **Error Handling:**  
   - Include a mechanism to display an error message if the file is missing or unavailable.  

---  

## Task 3 - Email Domains Pie Chart  
**File:** `assignment03-pie.ipynb`  
**Objective:** Generate a pie chart of email domains using the data from the CSV file available(https://drive.google.com/uc?id=1AWPf-pJodJKeHsARQK_RHiNsE8fjPCVK&export=download).  

### Explanation  
1. **Dataset Loading:**  
   - Fetch the data from the online CSV file and inspect it using `df.head()`.  

2. **Date Conversion:**  
   - Convert date strings to `datetime` objects for easier manipulation.  

3. **Age Calculation:**  
   - Calculate each person’s age by comparing their birthdate to the current date. Adjust for birthdays that haven’t occurred yet.  

4. **Age Grouping:**  
   - Bin ages into predefined ranges using `pd.cut()` and assign appropriate labels to these groups.  

5. **Visualization:**  
   - Use a pie chart to display the distribution of email domains. Include percentage labels for clarity.  

---  

## Task 5 - Risk Battle Simulation  
**File:** `assignment_5_risk.py` or `assignment_5_risk.ipynb`  
**Objective:** Simulate 1000 individual battle rounds in Risk (3 attackers vs 2 defenders) and visualize the results.  

### Rules of Risk  
- Each battle round involves rolling dice for the attacker and defender:  
  - The attacker rolls up to **3 dice** (3 troops).  
  - The defender rolls up to **2 dice** (2 troops).  
- Each side’s highest dice rolls are compared to determine the winner.  

### Explanation  
1. **Simulating Dice Rolls:**  
   - Use `np.random.randint` to generate random dice rolls for both attackers and defenders.  

2. **Finding the Winners:**  
   - Compare the highest dice roll from each side. The attacker wins if their roll is higher; otherwise, the defender wins.  

3. **Tracking Results:**  
   - Count the total wins for both attackers and defenders using `attacker_wins` and `defender_wins`.  

4. **Calculating Percentages:**  
   - Calculate the win percentages as `(wins / total battles) * 100`.  

5. **Visualizing Results:**  
   - Create the following visualizations:  
     - **Pie Chart:** Display the percentage of wins for attackers and defenders.  
     - **Bar Chart:** Show the absolute number of wins for each side.  

---  

## Task 6 - Weather Analysis  
**File:** `assignment_6_weather.py` or `assignment_6_weather.ipynb`  
**Objective:** Analyze and visualize temperature and wind speed trends using (https://cli.fusio.net/cli/climate_data/webdata/hly4935.csv).  

### Plots  
1. **Temperature Analysis:**  
   - Plot individual temperature readings.  
   - Calculate and plot the mean temperature for each day.  
   - Calculate and plot the mean temperature for each month.  

### Explanation  
1. **Load the Dataset:**  
   - Load the dataset from the given URL. Skip the first 23 rows (metadata or unrelated headers).  

2. **Data Conversion and Processing:**  
   - Convert the `date` column to a proper `datetime` format and normalize it to remove time details (hour and minute).  

3. **Temperature Analysis:**  
   - **Yearly Trends:** Group data by year (`YE`) to calculate and plot yearly average temperatures.  
   - **Monthly Trends:** Group data by month (`ME`) to calculate and plot monthly average temperatures.  

4. **Wind Speed Analysis:**  
   - Convert the `wdsp` (wind speed) column to numeric. Replace non-numeric values and zeros with `NaN`.  
   - Calculate the yearly and monthly average wind speeds.  

5. **Visualizations:**  
   - **Yearly Trends:** Line plots of yearly averages for temperature and wind speed.  
   - **Monthly Trends:** Line plots of monthly averages to highlight seasonal variations.  

---  
