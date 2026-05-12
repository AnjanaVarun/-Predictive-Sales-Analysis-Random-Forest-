# Predictive Sales Analysis: Carseats Revenue Strategy 🛒📈

## 📌 Project Overview
Retail sales for child car seats vary significantly by store. This project utilizes a Random Forest classification model to identify the socio-economic and store-level drivers of "High Sales" versus "Low Sales." By accurately predicting high-performing locations, the business can optimize inventory distribution, adjust competitive pricing, and effectively allocate targeted marketing spend.

## 📊 Dataset Description
The dataset contains sales data, competitor pricing, and local demographic information for 400 distinct retail locations.
* **Dataset Size:** 400 records, 11 variables.
* **Target Variable:** `Sales_Category` (Binary: "High Sales" vs. "Low Sales").
* **Key Features:** `CompPrice` (Competitor Price), `Income`, `Advertising`, `Population`, `Price`, `ShelveLoc` (Shelf Location Quality), `Age`, `Education`, `Urban`, `US`.

## 🛠️ Tech Stack
* **Language:** Python
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (Random Forest Classifier)
* **Data Visualization:** `matplotlib`, `seaborn`

## 🧠 Methodology & Model Development
1. **Exploratory Data Analysis (EDA):** Generated a **Count Plot of the target** to visualize the baseline distribution of High vs. Low performing stores. 
2. **Train/Test Split:** An **80/20 train-test split applied** to validate the model's predictive capabilities on unseen store data.
3. **Model Selection (Random Forest):** An ensemble Random Forest Classifier was chosen to seamlessly handle mixed data types (categorical variables like `ShelveLoc` and continuous pricing data) and extract complex, non-linear relationships.
4. **Feature Importance:** Generated a **Feature Importance bar chart** to rank the definitive drivers of retail success. 

## 📈 Key Results & Performance
The Random Forest ensemble achieved highly balanced, reliable forecasting across both performance categories.

* **Overall Accuracy Score:** `87.50%`
* **Detailed Classification Report (Test Size = 80):**
  * **High Sales:** Precision `0.88`, Recall `0.88`, F1-Score `0.88`
  * **Low Sales:** Precision `0.86`, Recall `0.86`, F1-Score `0.86`
* **Macro Average F1-Score:** `0.87`

## 💼 Business Impact & Inference
* **Precision Targeting:** A Precision of 0.88 for the "High Sales" class means that when the model flags a store as a top performer, it is correct 88% of the time. This drastically reduces "False Positives," ensuring the company does not waste premium inventory or targeted marketing budgets on stores that will ultimately underperform.
* **Key Takeaway (Execution > Demographics):** The Feature Importance analysis revealed that in-store execution is the primary growth lever. `ShelveLoc` (Shelf positioning) and competitive `Price` are vastly more predictive of sales volume than regional demographics like `Urban` vs. `Rural` status or local `Population`.
* **Next Steps:** Deploy the model to score prospective new retail partnerships. Additionally, run a separate regression pipeline to forecast exact continuous unit sales volumes rather than binary categories.
