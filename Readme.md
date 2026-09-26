# Fuel Economy Data Analysis

> A practical data analysis project using Fuel Economy data to investigate, clean, explore, visualize, and compare vehicle data from 2008 and 2018.

---

## 📌 Project Overview

This project follows a complete data-analysis workflow using Fuel Economy data provided by the U.S. Environmental Protection Agency (EPA), Office of Mobile Sources, National Vehicle and Fuel Emissions Laboratory.

The analysis works with two datasets:

- **2008 Fuel Economy Dataset**
- **2018 Fuel Economy Dataset**

The project covers data investigation, data assessment, cleaning, data-type correction, exploratory visualization, dataset merging, and answering analytical questions.

---
## 📁 Project Structure

```text
Fuel-Economy-Data-Analysis/
│
├── Fuel_Economy_Data/
│   ├── Readme.md
│   ├── all_alpha_08.csv
│   ├── all_alpha_18.csv
│   ├── clean_08.csv
│   ├── clean_18.csv
│   ├── combined_dataset.csv
│   └── data_08_v1.csv ... data_18_v4.csv
│
├── Data Analysis with Fuel Economy Data.ipynb
├── Description of economy fuel data.txt
├── Green Vehicle Guide Documentation.pdf
└── Readme.md
```

---

## 🎯 Project Objectives

The analysis investigates the following questions:

1. Are more models using alternative sources of fuel? By how much?
2. How much have vehicle classes improved in fuel economy?
3. What are the characteristics of SmartWay vehicles?
4. What features are associated with better fuel economy?
5. For models produced in 2008 that are still being produced in 2018, how much has MPG improved and which vehicle improved the most?

---

## 🛠️ Tools & Technologies

The notebook uses the following Python libraries:

- **Python**
- **Pandas** — data loading, cleaning, transformation, and analysis
- **NumPy** — numerical operations
- **Matplotlib** — data visualization
- **Jupyter Notebook** — interactive analysis environment

---

## 🔄 Analysis Workflow

The project follows this workflow:

```text
Investigate Data
      ↓
Ask Questions
      ↓
Assess Data
      ↓
Clean Data
      ↓
Fix Data Types
      ↓
Explore Data
      ↓
Create Visualizations
      ↓
Merge Datasets
      ↓
Analyze Results
      ↓
Conclude
```

---

## 📊 Dataset Overview

The notebook loads the two required CSV files using Pandas:

```python
import pandas as pd

df_08 = pd.read_csv('all_alpha_08.csv')
df_18 = pd.read_csv('all_alpha_18.csv')
```

The initial dataset dimensions are:

| Dataset | Rows | Columns |
|---|---:|---:|
| 2008 | 2,404 | 18 |
| 2018 | 1,611 | 18 |

---

## 🔍 Data Quality Assessment

The project assesses the datasets using operations such as:

- Checking dataset shape
- Inspecting the first records
- Checking duplicate records
- Checking missing/null values
- Inspecting data types
- Checking the number of unique values in each column

### Duplicate Records

The initial assessment identified:

| Dataset | Duplicate Records |
|---|---:|
| 2008 | 25 |
| 2018 | 0 |

### Missing Values

The assessment also identifies missing values before the cleaning stage.

For example, in the 2008 dataset, missing values were identified in fields including:

- Cyl
- Trans
- Drive
- FE Calc Appr
- City MPG
- Hwy MPG
- Cmb MPG
- Unadj Cmb MPG
- Greenhouse Gas Score

In the 2018 dataset, missing values were identified in:

- Displ
- Cyl

The notebook then continues with the required cleaning and transformation steps.

---

## 🧹 Data Cleaning

The project performs the following cleaning operations:

### 1. Drop Extraneous Columns

Columns that are not consistent between the datasets or are not required for the analysis are removed.

### 2. Rename Columns

Column names are standardized to make them easier to work with.

The project also makes the `Sales Area` and `Cert Region` naming consistent between the datasets.

### 3. Filter

Records are filtered based on the requirements of the analysis.

### 4. Drop Nulls

Rows containing required missing values are handled as part of the data-cleaning process.

### 5. Dedupe Data

Duplicate records are identified and removed where required.

### 6. Fixing Data Types

Data types are corrected for fields that were initially stored as objects but are required as numeric values for analysis.

The notebook specifically works with:

- `Cyl`
- `Air Pollution Score`
- `City MPG`
- `Hwy MPG`
- `Cmb MPG`
- `Greenhouse Gas Score`

---

## 📈 Exploring with Visuals

The project uses visualizations to explore the cleaned data and answer the analytical questions.

The visual exploration focuses on:

- Fuel types
- Vehicle classes
- Fuel economy
- SmartWay vehicles
- Vehicle characteristics
- MPG changes between 2008 and 2018

Visualizations are created using **Matplotlib**.

---

## 🔗 Dataset Comparison

The project compares the 2008 and 2018 datasets to identify changes in vehicle fuel economy and related characteristics.

The datasets are cleaned and standardized before they are combined for further analysis.

This allows models from different years to be compared using common attributes.

---

## 📁 Project Files

Only the following two CSV files need to be downloaded:

```text
all_alpha_08.csv
all_alpha_18.csv
```

All other datasets used in the project are generated while running the analysis code.

Recommended project structure:

```text
Fuel-Economy-Data-Analysis/
│
├── Data Analysis with Fuel Economy Data .ipynb
├── README.md
├── all_alpha_08.csv
└── all_alpha_18.csv
```

---

## ▶️ How to Run the Project

### Step 1 — Download the datasets

Download:

```text
all_alpha_08.csv
all_alpha_18.csv
```

### Step 2 — Place the files

Place both CSV files in the same directory as the Jupyter Notebook.

### Step 3 — Open the notebook

Open:

```text
Data Analysis with Fuel Economy Data .ipynb
```

using Jupyter Notebook or JupyterLab.

### Step 4 — Run the notebook

Run the cells in order, beginning with the data-import section.

---

## 📚 Original Project Documentation

The following sections contain the original project content and terminology.

---

## Table of Contents

* Know Data Attributes
* Ask Questions
* Assessing Data
* Clean Column Labels
* Filter, Drop Nulls, Dedupe
* Inspect Data Types
* Fixing Data Types
* Exploring with Visuals
* Merge Datasets
* Results with Merged Datasets

---

## What is Fuel Economy?

Excerpt from Wikipedia page on Fuel Economy in Automobiles:

The fuel economy of an automobile is the fuel efficiency relationship between the distance traveled and the amount of fuel consumed by the vehicle. Consumption can be expressed in terms of volume of fuel to travel a distance, or the distance travelled per unit volume of fuel consumed.

---

## Data set :

### Fuel Economy Data

This information is provided by the U.S. Environmental Protection Agency, Office of Mobile Sources, National Vehicle and Fuel Emissions Laboratory.

Note that the datasets we'll be working with are slightly simpler than those found through the links below.

* EPA Fuel Economy Testing : https://www.epa.gov/compliance-and-fuel-economy-data/data-cars-used-testing-fuel-economy
* DOE Fuel Economy Data : https://www.fueleconomy.gov/feg/download.shtml/

For better understanding of the dataset, you can refer the Green Vehicle Guide Documentation and data description.

---

## Attribute Description :

| Attribute | Description |
|---|---|
| Model | Vehicle make and model |
| Displ | Engine displacement - the size of an engine in liters |
| Cyl | The number of cylinders in a particular engine |
| Trans | Transmission Type and Number of Gears |
| Drive | Drive axle type (2WD = 2-wheel drive, 4WD = 4-wheel/all-wheel drive) |
| Fuel | Fuel Type |
| Cert Region* | Certification Region Code |
| Sales Area** | Certification Region Code |
| Stnd | Vehicle emissions standard code (View Vehicle Emissions Standards https://www.epa.gov/greenvehicles/federal-and-california-light-duty-vehicle-emissions-standards-air-pollutants) |
| Stnd Description* | Vehicle emissions standard description |
| Underhood ID | This is a 12-digit ID number that can be found on the underhood emission label of every vehicle. It's required by the EPA to designate its "test group" or "engine family." This is explained more here https://www.epa.gov/vehicle-and-engine-certification/information-about-family-naming-conventions-vehicles-and-engines |
| Veh Class | EPA Vehicle Class |
| Air Pollution Score | Air pollution score (smog rating) |
| City MPG | Estimated city mpg (miles/gallon) |
| Hwy MPG | Estimated highway mpg (miles/gallon) |
| Cmb MPG | Estimated combined mpg (miles/gallon) |
| Greenhouse Gas Score | Greenhouse gas rating |
| SmartWay | Yes, No, or Elite |
| Comb CO2* | Combined city/highway CO2 tailpipe emissions in grams per mile |

`*` means Not included in 2008 dataset

`**` means Not included in 2018 dataset

---

## 📖 Additional Dataset Documentation

The project includes supporting documentation for understanding the Fuel Economy data attributes.

The Green Vehicle Guide documentation defines fields including Model, Displ, Cyl, Trans, Drive, Fuel, Cert Region, Stnd, Veh Class, Air Pollution Score, City MPG, Hwy MPG, Cmb MPG, Greenhouse Gas Score, SmartWay, and Comb CO2. fileciteturn0file1L2-L6 fileciteturn0file1L25-L36

The documentation also provides definitions for emissions-related and fuel-economy fields such as Air Pollution Score, City MPG, Hwy MPG, Cmb MPG, Greenhouse Gas Score, SmartWay, and Comb CO2. fileciteturn0file1L38-L52

---

## 💡 Key Skills Demonstrated

This project demonstrates practical experience with:

- Data loading using Pandas
- Data inspection
- Data-quality assessment
- Missing-value handling
- Duplicate detection and removal
- Column standardization
- Data-type conversion
- Filtering and transformation
- Exploratory data analysis
- Data visualization
- Dataset merging
- Comparative analysis
- Drawing conclusions from data

---

## 📌 Project Summary

This project demonstrates an end-to-end approach to working with real-world Fuel Economy data.

The analysis moves from understanding the dataset and identifying questions to assessing data quality, cleaning and transforming the data, exploring patterns through visualization, comparing different model years, and communicating the results.

---

## 📎 Data Availability Note

When you do this project, you only need to download two CSV files:

```text
all_alpha_08.csv
all_alpha_18.csv
```

All the rest datasets will be generated during the codes running.

---

## 📜 Data Source

The Fuel Economy information is provided by the U.S. Environmental Protection Agency, Office of Mobile Sources, National Vehicle and Fuel Emissions Laboratory. The project documentation also references the EPA Fuel Economy Testing and DOE Fuel Economy Data resources.

---
