# Student Performance Analysis & Machine Learning

## Project Overview

This project analyzes student performance using the **Student Performance Dataset** and applies basic machine learning techniques to predict students' final grades.

The project covers data cleaning, exploratory data analysis (EDA), data visualization, correlation analysis, and linear regression.

## Dataset

The dataset contains information about students taking a Portuguese language course.

Some of the important features include:

* `sex` — student's gender
* `age` — student's age
* `studytime` — weekly study time
* `failures` — number of previous class failures
* `absences` — number of school absences
* `G1` — first-period grade
* `G2` — second-period grade
* `G3` — final grade

The original dataset is from the **UCI Student Performance Dataset**.

## Data Analysis

The following questions were investigated:

* Number of students and columns
* Missing values
* Duplicate rows
* Average, minimum, and maximum final grades
* Distribution of students by gender
* Percentage of students with internet access
* Average final grade for different study-time groups
* Relationship between absences and final grade
* Relationship between previous grades (`G1`, `G2`) and final grade (`G3`)
* Factors most strongly correlated with final grade

## Visualizations

The project includes visualizations such as:

* Study time vs final grade
* Absences vs final grade
* `G2` vs `G3`
* Average `G3` by gender

## Machine Learning

### Model 1 — Linear Regression

The first model predicts the final grade (`G3`) using:

```text
studytime
failures
absences
G1
G2
```

The data was divided into training and testing sets using an 80/20 split.

### Model 2 — Linear Regression Without Previous Grades

A second model was trained using only:

```text
studytime
failures
absences
```

The two models were compared using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* R² Score

This comparison helps determine how much predictive information is provided by previous grades (`G1` and `G2`).

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

## Project Structure

```text
student-performance-analysis/
│
├── student-por.csv
├── student_performance.ipynb
└── README.md
```

## How to Run

Clone the repository:

```bash
git clone https://github.com/hammadurrehmantariq/student-performance-analysis.git
```

Navigate into the project directory:

```bash
cd student-performance-analysis
```

Install the required libraries:

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

Open the notebook:

```bash
jupyter notebook
```

Then open `student_performance.ipynb`.

## Key Learning Outcomes

Through this project, I practiced:

* Loading and inspecting datasets with Pandas
* Handling and checking missing data
* Detecting duplicate records
* Grouping and aggregating data
* Creating data visualizations
* Measuring correlations
* Splitting data into training and testing sets
* Training a Linear Regression model
* Making predictions
* Evaluating machine learning models using MAE, MSE, and R²
* Comparing different feature sets

## Future Improvements

Possible improvements include:

* Trying additional machine learning models such as Random Forest
* Feature engineering
* Hyperparameter tuning
* Creating an interactive dashboard using Power BI
* Improving model evaluation with cross-validation
