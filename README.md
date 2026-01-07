# RetailAI: Online Shopper Intent & Revenue Prediction

## 📌 Project Overview

In the competitive landscape of e-commerce, understanding user behavior in real-time is critical. This project, **RetailAI**, utilizes machine learning to analyze the "Online Shoppers Purchasing Intention" dataset. By examining session metrics—such as page dwell time, bounce rates, and visitor types—this model predicts whether a browsing session will result in a purchase (**Revenue**).

The goal is to provide actionable insights that help retailers optimize their conversion funnels and target high-intent customers more effectively.

## 📊 The Dataset

The analysis is performed on a dataset consisting of **12,330 sessions**. Each session is characterized by 18 features, categorized into:

* **Session Metrics:** Administrative, Informational, and Product Related page views and durations.
* **Web Analytics:** Bounce Rates, Exit Rates, and Page Values.
* **Temporal Factors:** Month of the year, Special Days (e.g., proximity to Mother's Day or Valentine's Day), and Weekend browsing.
* **User Demographics:** Operating system, Browser type, Region, and Visitor Type (New vs. Returning).

## 🛠️ Tech Stack

* **Language:** Python
* **Libraries:** * `Pandas` & `NumPy` for data manipulation.
* `Scikit-Learn` for machine learning and evaluation.
* `Imbalanced-Learn (SMOTE)` to handle class imbalance in purchase data.
* `Seaborn` & `Matplotlib` for exploratory data analysis (EDA).



## 🚀 Key Workflow

1. **Exploratory Data Analysis (EDA):** Identified key correlations, such as the high impact of `PageValues` on conversion and how `ExitRates` negatively correlate with revenue.
2. **Data Preprocessing:** * Handled categorical encoding for features like `Month` and `VisitorType`.
* Removed duplicate entries to ensure model integrity.
* Standardized numerical features for better model convergence.


3. **Handling Class Imbalance:** Since most browsing sessions do not end in a purchase, we employed **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset, ensuring the model doesn't just "guess" no-purchase.
4. **Modeling:** Implemented a **Decision Tree Classifier** within a robust pipeline to predict the binary `Revenue` target.

## 📈 Insights & Results

* **Page Value is King:** Users who visit pages with higher internal values are significantly more likely to complete a purchase.
* **Engagement Matters:** There is a clear threshold where the time spent on "Product Related" pages correlates with higher intent.
* **Performance:** The model effectively balances Precision and Recall, providing a reliable baseline for identifying potential buyers before they leave the site.

## 📂 Project Structure

```bash
├── AI_IN_RETAIL_GRP_PROJECT.ipynb  # Main Analysis & Modeling Notebook
├── README.md                        # Project Documentation
└── online_shoppers_intention.csv    # Dataset (Source: Kaggle)

```

## ⚙️ How to Run

1. Clone the repository:
```bash
git clone https://github.com/priiyanshuraj/retailai.git

```


2. Install dependencies:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn

```


3. Open the Jupyter Notebook:
```bash
jupyter notebook AI_IN_RETAIL_GRP_PROJECT.ipynb

```



---

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
**Author:** Priyanshu Raj
