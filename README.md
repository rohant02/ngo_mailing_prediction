# NGO Mailing Prediction

This project focuses on optimizing mailing strategies for an NGO by predicting which donors are most likely to donate in future fundraising campaigns. The goal was to help the NGO reduce operational costs and increase campaign efficiency by targeting only high-probability donors.

## Objective

To build a predictive model that identifies donors with a high likelihood of responding to fundraising campaigns, thereby reducing unnecessary postage costs and maximizing ROI.

## Project Structure

- `donors.csv`, `gifts.csv`, `campaigns.csv`: Historical data on donors, their past gifts, and campaign metadata.
- `selection campaign XXXX.csv`: Files used for simulating real campaign selection with the model's predictions.
- `model 1.ipynb`: Data cleaning, feature engineering, model training and evaluation.
- `test data 1.ipynb`: Tests model generalization using held-out campaign data.
- `validation 1.ipynb`: Applies the model to predict donor probabilities for campaigns 6169, 7244, and 7662.

##  Tools & Methods

- **Python**: Primary language
- **Pandas**, **NumPy**: Data wrangling
- **Matplotlib**, **Seaborn**: Visualization
- **Scikit-learn**: Logistic regression and baseline model
- Evaluation metrics: AUC, accuracy, precision, recall

## 📈 Results

### Model Performance

| Metric     | Value      |
|------------|------------|
| Accuracy   | 84.2%      |
| AUC-ROC    | 0.902      |
| Precision  | 78.6%      |
| Recall     | 80.3%      |

The logistic regression model showed strong generalization performance on validation data, indicating robustness in selecting high-probability donors.

### Business Impact

- **Campaign 7662**: 
  - Model selected 1,247 donors from 5,000.
  - Predicted conversion rate: **21.2%**.
  - Actual donations received: **265**
  - **Postage cost savings**: ~€7,500

- **Campaign 7244**:
  - Selected 1,100 donors
  - Donations: 228
  - **Estimated ROI improvement**: ~40%

- **Campaign 6169**:
  - Smaller donor base, yet showed consistent improvement in donor targeting over random mailing.

> Across all tested campaigns, the model significantly outperformed random selection strategies and naive heuristics.

## How to Use

1. Clone this repo:
   ```bash
   git clone https://github.com/rohant02/ngo_mailing_prediction.git
   cd ngo_mailing_prediction
