# Insurance Cost Regression

A comprehensive machine learning project that performs end-to-end analysis of medical insurance data, including exploratory data analysis, feature engineering, and predictive modeling using linear regression to estimate insurance costs based on various demographic and health factors.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Methodology](#methodology)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [License](#license)
- [Contributing](#contributing)

## Overview

This project aims to predict medical insurance costs using machine learning techniques. The analysis includes thorough data exploration, statistical testing for feature selection, data preprocessing, and the development of a linear regression model. The project demonstrates practical application of data science workflows, from raw data analysis to model deployment.

## Dataset

The dataset used in this project contains medical insurance information with the following features:

- **age**: Age of the primary beneficiary
- **sex**: Gender of the insurance contractor (male/female)
- **bmi**: Body mass index, providing an understanding of body weight relative to height
- **children**: Number of children covered by health insurance
- **smoker**: Smoking status (yes/no)
- **region**: Residential area in the US (northeast, southeast, southwest, northwest)
- **charges**: Individual medical costs billed by health insurance (target variable)

The dataset is loaded directly from a public GitHub repository and contains no missing values.

## Installation

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/003shrey/Insurance-Cost-Regression.git
cd Insurance-Cost-Regression
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

Alternatively, you can install packages individually:
```bash
pip install numpy pandas seaborn matplotlib scikit-learn scipy jupyter
```

## Usage

1. Launch Jupyter Notebook:
```bash
jupyter notebook
```

2. Open the `Insurance_Cost_Prediction.ipynb` notebook in your browser.

3. Run all cells sequentially to:
   - Load and explore the data
   - Perform exploratory data analysis
   - Engineer new features
   - Train the linear regression model
   - Evaluate model performance

## Project Structure

```
Insurance-Cost-Regression/
│
├── Insurance_Cost_Prediction.ipynb    # Main Jupyter notebook with complete analysis
├── requirements.txt                   # Python package dependencies
├── README.md                          # Project documentation
└── LICENSE                            # MIT License file
```

## Methodology

The project follows a systematic approach to building a predictive model:

### 1. Exploratory Data Analysis (EDA)
- Statistical summary of numerical and categorical variables
- Distribution analysis using histograms and count plots
- Outlier detection using box plots
- Correlation analysis using heatmaps

### 2. Data Preprocessing
- Handling duplicate records
- Encoding categorical variables (sex, smoker status)
- One-hot encoding for multi-class features (region)
- Feature engineering: BMI categorization (Underweight, Normal, Overweight, Obese)

### 3. Feature Selection
- Pearson correlation analysis for numerical features
- Chi-square test of independence for categorical features
- Statistical significance testing with alpha = 0.05

### 4. Data Transformation
- Standard scaling of numerical features (age, bmi, children)
- Final feature set selection based on statistical tests

### 5. Model Development
- Train-test split for model validation
- Linear regression model training
- Model evaluation using R-squared score

## Results

The linear regression model provides insights into the factors that significantly influence insurance costs. Key findings include:

- Smoking status is a strong predictor of insurance charges
- Age and BMI show positive correlation with insurance costs
- Regional variations and BMI categories contribute to cost predictions
- The model performance is evaluated using R-squared metrics

## Technologies Used

- **Python**: Primary programming language
- **NumPy**: Numerical computing
- **Pandas**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical data visualization
- **Scikit-learn**: Machine learning algorithms and preprocessing
- **SciPy**: Statistical functions and hypothesis testing
- **Jupyter**: Interactive development environment

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome. If you would like to contribute to this project, please follow these steps:

1. Fork the repository
2. Create a new branch for your feature (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

For major changes, please open an issue first to discuss what you would like to change.

---

For questions or feedback, please open an issue in the repository.
