# House Sales Analysis in King County, USA

## Project Overview
This project analyzes house sales in King County, USA, using Python. The dataset includes house sale prices from May 2014 to May 2015, covering features like the number of bedrooms, bathrooms, square footage, and more. The primary goal is to explore the data, handle missing values, visualize key insights, and build predictive models to estimate house prices.

---

## Table of Contents
1. [Dataset](#dataset)
2. [Features](#features)
3. [Installation](#installation)
4. [Modules Covered](#modules-covered)
5. [Usage](#usage)
6. [Results](#results)
7. [License](#license)

---

## Dataset
The dataset contains 21 features related to houses sold in King County, Washington. It includes details such as square footage, the number of bedrooms, and sale prices. The dataset is used to perform exploratory data analysis, data cleaning, and machine learning tasks.

---

## Features
| **Feature**          | **Description**                                                                 |
|-----------------------|---------------------------------------------------------------------------------|
| `id`                 | Unique ID for each house                                                       |
| `date`               | Date the house was sold                                                        |
| `price`              | Sale price of the house (target variable)                                      |
| `bedrooms`           | Number of bedrooms                                                             |
| `bathrooms`          | Number of bathrooms                                                            |
| `sqft_living`        | Square footage of the living area                                              |
| `sqft_lot`           | Square footage of the lot                                                     |
| `floors`             | Number of floors                                                              |
| `waterfront`         | Indicates if the house has a waterfront view                                   |
| `view`               | Indicates if the house has been viewed                                        |
| `condition`          | Overall condition of the house                                                |
| `grade`              | Overall grade based on King County grading system                             |
| `sqft_above`         | Square footage above ground                                                   |
| `sqft_basement`      | Square footage of the basement                                                |
| `yr_built`           | Year the house was built                                                      |
| `yr_renovated`       | Year the house was renovated                                                  |
| `zipcode`            | ZIP code of the location                                                      |
| `lat`                | Latitude coordinate                                                           |
| `long`               | Longitude coordinate                                                          |
| `sqft_living15`      | Living room area in 2015                                                      |
| `sqft_lot15`         | Lot area in 2015                                                              |

---

## Installation

To run the project, ensure you have Python installed along with the required libraries. You can install the libraries using:

## Steps Involved:

1. Data Wrangling
Loaded the dataset and cleaned missing values in bedrooms and bathrooms by replacing them with the mean.
Dropped unnecessary columns (id and Unnamed: 0).

3. Exploratory Data Analysis
Counted houses with unique floor values.
Used box plots to analyze waterfront houses.
Performed correlation analysis to identify features most correlated with price.

5. Model Development
Built linear regression models:
Predicting price using individual features like sqft_living (R² = 0.49).
Using multiple features to predict price (R² = 0.66).
Created pipelines for polynomial regression and evaluated performance using Ridge Regression.

7. Model Evaluation and Refinement
Split data into training and testing sets.
Applied Ridge regression with second-order polynomial features, achieving an R² = 0.70.

## Clone the repository:
git clone https://github.com/your-username/king-county-house-sales.git
cd king-county-house-sales

### Load the dataset: Download the dataset from the provided link or load it directly using:
df = pd.read_csv("kc_house_data_NaN.csv")

### Run the analysis:
Use Jupyter Notebook or Python to execute the analysis.

Count houses with unique floor values:
df['floors'].value_counts().to_frame()

Box plot for price outliers:
sns.boxplot(x='waterfront', y='price', data=df)

Regression model with polynomial features:
RidgeModel1.fit(x_train_pr, y_train)
RidgeModel1.score(x_test_pr, y_test)

## Results

Correlation Analysis:
Features most correlated with price:
sqft_living (0.70)
grade (0.66)
sqft_above (0.60)

Model Performance:
Simple Linear Regression (sqft_living): R² = 0.49
Multiple Linear Regression: R² = 0.66
Ridge Regression with Polynomial Features: R² = 0.70

Insights:
Houses with waterfront views tend to have more price outliers.
Larger sqft_living and higher grade strongly influence house prices.

License:
This project is licensed under the MIT License.

Author

Shivani Kanodia
Role: Data Analyst / Data Scientist
GitHub: Your GitHub Profile
Contribution

Contributions are welcome! Please open an issue or submit a pull request.


---

### **Steps to Use This README**
1. Copy the content into a file named `README.md` in your project directory.
2. Add any images (like plots) referenced in the README, and update their paths in the file.
3. Push the changes to your GitHub repository.

Let me know if you'd like additional customization or help uploading it to GitHub!
