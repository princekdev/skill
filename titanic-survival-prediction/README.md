# Titanic Survival Prediction – Data Cleaning & Basic ML

**Skill Nexis ML & AI Internship — Week 1 Project**
**Author:** Prince Kumar

## Project Description

This project is a beginner-level, end-to-end Machine Learning workflow built on the
classic Titanic dataset. It covers loading raw data, exploring it, cleaning missing
values, encoding categorical features, visualizing a key feature, and training a
simple Logistic Regression model to predict whether a passenger survived the Titanic
disaster. It was built to satisfy the Week 1 learning requirements of the Skill Nexis
ML & AI internship, following the fundamentals covered in Programming with Mosh's
*"Python Machine Learning Tutorial (Data Science)"*.

## Dataset Used

The [Titanic dataset](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv)
(publicly hosted on GitHub by Data Science Dojo), containing 891 passenger records
with details such as age, sex, ticket class, fare, and survival outcome. The notebook
loads the dataset directly from this URL, so no manual download is required.

## Technologies / Libraries Used

- Python 3
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn (`LabelEncoder`, `train_test_split`, `LogisticRegression`, metrics)
- Jupyter Notebook

## Main Steps Performed

1. Loaded the Titanic dataset with pandas from a public URL.
2. Inspected the data (`head()`, `shape`, `info()`, `describe()`).
3. Identified missing values across all columns.
4. Cleaned the data:
   - Filled missing `Age` with the median.
   - Filled missing `Embarked` with the mode.
   - Converted `Cabin` into a binary `Has_Cabin` feature and dropped the original column.
   - Dropped non-predictive columns: `PassengerId`, `Name`, `Ticket`.
5. Encoded categorical features:
   - Label-encoded `Sex`.
   - One-hot encoded `Embarked`.
6. Engineered a simple `FamilySize` feature from `SibSp` and `Parch`.
7. Visualized the Age distribution with a histogram/KDE plot.
8. Defined features (`X`) and target (`y = Survived`).
9. Split the data into training (80%) and testing (20%) sets.
10. Trained a Logistic Regression classification model.
11. Evaluated the model using accuracy, a confusion matrix, and a classification report.
12. Saved the cleaned dataset to `data/titanic_cleaned.csv`.

## How to Run the Notebook

1. Clone or download this repository.
2. (Recommended) Create and activate a virtual environment.
3. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
4. Launch Jupyter Notebook:
   ```bash
   jupyter notebook notebooks/PrinceKumar_Titanic_Survival_Analysis.ipynb
   ```
5. Run all cells from top to bottom (**Kernel → Restart & Run All**). The notebook
   downloads the dataset automatically and will regenerate `data/titanic_cleaned.csv`.

## Result / Accuracy Obtained

The Logistic Regression model achieved an accuracy of **≈ 80.4%** on the held-out
test set (20% of the data). Exact results may vary slightly depending on library
versions, but should remain close to this figure since `random_state=42` is used for
reproducibility.

## Project Structure

```text
titanic-survival-prediction/
├── data/
│   └── titanic_cleaned.csv
├── notebooks/
│   └── PrinceKumar_Titanic_Survival_Analysis.ipynb
├── README.md
└── requirements.txt
```
