# SecureFlow

## Project Overview

Anomaly detection is crucial for identifying unusual patterns in credit card transactions, which could indicate fraudulent activity. This project aims to detect anomalies in credit card transactions using machine learning techniques. The goal is to flag transactions that deviate significantly from typical behavior.

## Kaggle Notebook

Explore the analysis and model development in this [Kaggle Notebook](https://www.kaggle.com/code/sugataghosh/anomaly-detection-in-credit-card-transactions).

## Dataset

**Source:** [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)

The dataset includes credit card transactions from European cardholders over two days in September 2013. It consists of 284,807 transactions, with 492 labeled as fraudulent. This highly imbalanced dataset features:

- **Time:** Time in seconds since the first transaction.
- **V1 to V28:** PCA-transformed features derived from confidential original data.
- **Amount:** Transaction amount.
- **Class:** Transaction authenticity (0 for legitimate, 1 for fraudulent).

## Project Objective

The primary objective is to build an anomaly detection system that identifies fraudulent transactions based on `Time`, `Amount`, and PCA-transformed features (`V1` to `V28`). The approach involves:

1. **Feature Extraction and Transformation:** Preparing and transforming features to handle high-dimensional data effectively.
2. **Dimensionality Reduction:** Selecting relevant features to distinguish between legitimate and fraudulent transactions.
3. **Modeling:** Fitting a multivariate normal distribution to the training data. Transactions are flagged as fraudulent if their density under this distribution is below a specific threshold.
4. **Evaluation:** Optimizing the threshold to maximize the F2-score, which minimizes false negatives (missed fraudulent transactions). The threshold is tuned based on validation set performance.

## Results

- **Optimal Threshold:** Approximately \(3.87 \times 10^{-19}\)
- **F2-score on Validation Set:** 0.834671
- **F2-score on Test Set:** 0.816492

## Getting Started

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/anomaly-detection-credit-card-transactions.git
    cd anomaly-detection-credit-card-transactions
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the analysis:
    ```bash
    python main.py
    ```

## Prerequisites

- Basic knowledge of Python programming.
- Understanding of database CRUD operations.
- Familiarity with data analysis and machine learning concepts.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions or feedback, please open an issue or contact [Your Name](mailto:your.email@example.com).
