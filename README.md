# Programming-Assignment-3
A collection of python codes focusing on data loading, indexing, slicing, and subsetting. This includes solutions for exploring a dataset of cars and extracting specific information using Pandas operations.  

---

## 📋 The Problems  

### 1. Problem 1: Data Loading and Exploration  
**File:** `Surname_Pandas-P1.py`  

**Task:**  
- Load the provided `.csv` file into a Pandas DataFrame named `cars`.  
- Display the first five rows and the last five rows of the dataset.  

**Example Code:**  
```python
import pandas as pd  

cars = pd.read_csv('cars.csv')  
print(cars.head())  
print(cars.tail())
```

### 2. Problem 2: Data Extraction with Pandas
**File:** `Surname_Pandas-P2.py`

**Task:**
Using the dataframe cars from Problem 1, perform the following:
- Display the first five rows with odd-numbered columns (1, 3, 5, 7...).
- Display the row that contains the Model = ‘Mazda RX4’.
- Find how many cylinders (‘cyl’) the car model ‘Camaro Z28’ has.
- Determine the cylinders (‘cyl’) and gear type (‘gear’) of the car models:
  ‘Mazda RX4 Wag’
  ‘Ford Pantera L’
  ‘Honda Civic’

**Example Code:**
```python
import pandas as pd  

cars = pd.read_csv('cars.csv')  

# 1. First five rows with odd-numbered columns
print(cars.iloc[:5, ::2])  

# 2. Row that contains the Model = 'Mazda RX4'
print(cars.loc[cars['Model'] == 'Mazda RX4'])  

# 3. Cylinders of 'Camaro Z28'
print(cars.loc[cars['Model'] == 'Camaro Z28', ['cyl']])  

# 4. Cylinders and gear type of selected models
models = ['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']  
print(cars.loc[cars['Model'].isin(models), ['Model', 'cyl', 'gear']])
```

