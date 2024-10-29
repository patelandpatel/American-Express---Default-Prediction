# American-Express---Default-Prediction
# American Express - Default Prediction

American Express is a globally integrated payments company and the largest payment card issuer in the world. The objective of this project is to predict the probability that a customer does not pay back their credit card balance amount in the future based on their monthly customer profile. The target binary variable is calculated by observing an 18-month performance window after the latest credit card statement, and if the customer does not pay the due amount in 120 days after their latest statement date, it is considered a default event.

## Repository Structure

- **`american_express_default_prediction.ipynb`**: A Jupyter notebook that provides a step-by-step implementation of a model to predict credit card payment defaults.
- **Data**: The dataset containing aggregated customer profiles at each statement date. Features are anonymized and normalized.

## Dataset Description

The dataset contains aggregated profile features for each customer at each statement date. Features fall into the following general categories:

- **D_***: Delinquency variables
- **S_***: Spend variables
- **P_***: Payment variables
- **B_***: Balance variables
- **R_***: Risk variables

The following features are categorical:

`['B_30', 'B_38', 'D_114', 'D_116', 'D_117', 'D_120', 'D_126', 'D_63', 'D_64', 'D_66', 'D_68']`

## Evaluation Metric

The evaluation metric for this competition is the mean of two measures of rank ordering: the Normalized Gini Coefficient (G) and the default rate captured at 4% (D). The metric (M) is calculated as follows:

```
M = 0.5 * (G + D)
```

The default rate captured at 4% is the percentage of the positive labels (defaults) captured within the highest-ranked 4% of the predictions, representing a Sensitivity/Recall statistic. For both sub-metrics G and D, the negative labels are given a weight of 20 to adjust for downsampling.

The maximum value for this metric is 1.0.

## Getting Started

### Prerequisites

- Python 3.7 or later
- Jupyter Notebook
- Required Python libraries:
  - Pandas
  - NumPy
  - Scikit-Learn
  - XGBoost
  - Matplotlib

You can install the necessary libraries by running:
```sh
pip install pandas numpy scikit-learn xgboost matplotlib
```

### Running the Notebook

1. Clone the repository:
   ```sh
   git clone <repository-url>
   ```
2. Navigate to the repository directory:
   ```sh
   cd <repository-directory>
   ```
3. Open the Jupyter notebook:
   ```sh
   jupyter notebook american_express_default_prediction.ipynb
   ```
4. Follow the steps in the notebook to preprocess the data, train the model, and evaluate performance.

## Project Overview

The goal of this project is to predict whether a customer will default on their credit card payments. The project utilizes machine learning techniques to analyze customer profiles and make predictions based on historical data.

### Key Steps:

- **Data Preprocessing**: Load and preprocess the dataset, handle missing values, and normalize features.
- **Feature Engineering**: Create meaningful features that help in improving model performance.
- **Model Training**: Train machine learning models such as logistic regression, XGBoost, etc., to predict the probability of default.
- **Model Evaluation**: Use the provided evaluation metric to assess model performance.

## Contributing

Contributions are welcome! If you have suggestions for improving the code or adding new features, please feel free to open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.



