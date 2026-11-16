# ⚡ Electricity Usage Predictor
### Problem Statement No. 61

A Python-based Electricity Usage Prediction System that analyzes historical electricity consumption data and predicts future electricity usage using **Linear Regression**.

The project uses Pandas, NumPy, and Matplotlib for data processing, mathematical calculations, prediction, and visualization.

---

## 📌 Project Overview

The Electricity Usage Predictor is a simple data analysis and prediction application designed to estimate future electricity consumption based on previously recorded monthly usage.

It reads electricity consumption data from a CSV file, analyzes the available records, builds a Linear Regression model, and predicts electricity usage for a user-specified month.

It also calculates the estimated electricity bill based on a fixed rate of ₹6 per unit and displays a graph comparing actual and predicted consumption.

## ✨ Features

- **CSV Data Import:** Reads monthly electricity usage from a CSV file.
- **Data Validation:** Detects and removes missing or invalid data.
- **Data Analysis:** Calculates total, average, minimum, and maximum electricity consumption.
- **Linear Regression:** Builds a prediction model using NumPy.
- **Future Prediction:** Predicts electricity consumption for a selected month.
- **Bill Estimation:** Calculates the estimated electricity bill at ₹6 per unit.
- **R² Score:** Displays the model's coefficient of determination.
- **Data Visualization:** Generates a graph showing actual usage, regression line, and predicted usage.
- **Interactive Menu:** Provides options to predict electricity consumption or exit the application.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | CSV handling and data analysis |
| NumPy | Mathematical calculations and Linear Regression |
| Matplotlib | Graphs and data visualization |

## 📂 Project Structure

```text
Electricity-Usage-Predictor/
│
├── electricity_predictor.py   # Main Python program
├── usage.csv                  # Electricity usage dataset
├── README.md                  # Project documentation
└── requirements.txt           # Required Python libraries
```

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Electricity-Usage-Predictor.git
```

### 2. Navigate to the Project Folder

```bash
cd Electricity-Usage-Predictor
```

### 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib
```

Alternatively, create a `requirements.txt` file:

```text
pandas
numpy
matplotlib
```

Then install dependencies:

```bash
pip install -r requirements.txt
```

### 4. Run the Application

```bash
python electricity_predictor.py
```

## 📊 Dataset Format

The application requires a CSV file containing exactly two columns:

- `Month` – Month number.
- `Units` – Electricity consumed in units (kWh).

**Example: `usage.csv`**

```csv
Month,Units
1,120
2,135
3,150
4,145
5,170
6,180
7,195
8,210
9,205
10,225
```

**Note:** The program supports CSV files both with and without a header row. Invalid or missing values are automatically removed with a warning.

## 🧠 How It Works

The project follows these steps:

1. **Data Loading:** Imports electricity consumption records from the CSV file using Pandas.
2. **Data Cleaning:** Converts the Month and Units columns into numeric values and removes invalid records.
3. **Data Analysis:** Calculates basic statistical information about electricity consumption.
4. **Model Training:** Uses NumPy's `polyfit()` function to calculate the slope and intercept of a Linear Regression model.
5. **Prediction:** Estimates electricity consumption for the selected month.
6. **Bill Calculation:** Multiplies predicted units by the electricity rate.
7. **Visualization:** Uses Matplotlib to display actual consumption and predicted consumption.

### Linear Regression Formula

The project uses the following equation:

```text
Y = mX + c
```

Where:

- `Y` = Predicted electricity consumption
- `X` = Month number
- `m` = Slope of the regression line
- `c` = Intercept

### Electricity Bill Formula

```text
Estimated Bill = Predicted Units × Rate
```

**Electricity Rate = ₹6 per unit**

## 🖥️ Sample Output

```text
Enter CSV file name (default usage.csv):

--- Data Summary ---
Header row detected and skipped.
Rows read      : 10
Valid rows     : 10
Total units    : 1735
Average units  : 173.5
Min / Max units: 120 / 225

===== Electricity Usage Predictor =====
1. Predict
2. Exit

Enter your choice: 1

Enter month number to predict: 11

Slope: 11.27 | Intercept: 108.00 | R2: 0.99

Predicted units (Month 11): 232.00
Estimated bill: Rs. 1392.00
```

*Note: Sample output values are illustrative. Actual results depend on the dataset.*

## 📈 Graphical Visualization

The application generates a graph containing:

- **Blue Dots:** Actual electricity consumption.
- **Red Line:** Linear Regression line.
- **Green Star:** Predicted electricity consumption.

The graph helps users understand historical electricity usage and the predicted trend.

## ⚠️ Important Notes

- At least two valid months of data are required for prediction.
- Month numbers must be positive whole numbers.
- The CSV file must contain exactly two columns.
- The electricity rate is currently fixed at ₹6 per unit.
- Predictions are estimates based on historical trends and may differ from actual consumption.
- The model assumes a linear relationship between month number and electricity consumption.

## 🚀 Future Improvements

- Add machine learning algorithms for improved prediction.
- Allow users to customize electricity rates.
- Support larger historical datasets.
- Add monthly and yearly consumption reports.
- Develop a graphical user interface (GUI).
- Build a web-based electricity prediction dashboard.

## 🎯 Project Objective

The main objective of this project is to demonstrate how Python libraries and basic machine learning concepts can be used to analyze historical electricity consumption, predict future usage, and estimate electricity bills.

---

**Project:** Electricity Usage Predictor  
**Problem Statement:** PS No. 61  
**Language:** Python  
**Libraries:** Pandas, NumPy, Matplotlib  
**Prediction Technique:** Linear Regression

**Developed as an academic Python project.**
