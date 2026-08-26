# Predicting Pharma Ad Performance

Break Through Tech AI Studio Challenge Project, Fall 2026
Host company: **WebMD** | Team: **Pharma 1A**

Forecasting second half pharmaceutical campaign performance from January through June historical data.

---

### 👥 **Team Members**

| Name | GitHub Handle | Contribution |
|------|---------------|--------------|
| Rhea Coulthurst John | @Qurash13 | *To be updated* |
| Nida Syed | *TBD* | *To be updated* |
| Abhi Segu | *TBD* | *To be updated* |
| Bakari Kerr | *TBD* | *To be updated* |
| Emma Zhang | *TBD* | *To be updated* |
| Tim Hsu | *TBD* | *To be updated* |

### 🧭 **Program Support**

| Role | Name |
|------|------|
| AI Studio Coach | Anushka Naik |
| Challenge Advisor | Kimia Naeiji |

Biweekly check ins are held with our Challenge Advisor.

**Project links**

- [Challenge Project Overview](./Challenge-Project-Overview.md)
- [Break Through Tech source repository](https://github.com/Break-Through-Tech/Pharma-1A-predicting-pharma-ad-performance)

---

## 🎯 **Project Highlights**

- Building regression models to predict **total spend**, **cost per engagement (CPE)**, and **engagement volume** for second half pharmaceutical campaigns on WebMD.
- Predictions are broken out by **tactic type**, **client segment**, and **healthcare professional specialty**.
- Target performance on the held out H2 test set: **MAPE below 30 percent** and **R² above 0.55**.
- Beyond raw accuracy, the work surfaces which campaign characteristics drive higher CPE, for example specialty, tactic, and geography combinations, so the findings translate into media planning decisions.
- Every data decision, model choice, and evaluation step is documented in a reproducible notebook.

---

## 👩🏽‍💻 **Setup and Installation**

*To be completed as the codebase develops.* Planned contents of this section:

1. **Clone the repository**
   ```bash
   git clone https://github.com/Qurash13/Pharma-1A-predicting-pharma-ad-performance.git
   cd Pharma-1A-predicting-pharma-ad-performance
   ```
2. **Create the environment**
   ```bash
   python -m venv venv
   source venv/bin/activate      # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```
3. **Core libraries:** pandas, scikit-learn, XGBoost, SHAP, matplotlib, seaborn
4. **Dataset access:** *provided by WebMD through the AI Studio program, instructions to be added*
5. **Run the notebooks** in `notebooks/` in numbered order

---

## 🏗️ **Project Overview**

This project is part of the **Break Through Tech AI Program**, a national initiative that pairs undergraduate students with industry partners for a semester long applied machine learning studio. Teams work alongside an AI Studio Coach and a Challenge Advisor from the host company to deliver a real solution to a real business problem.

Our host company is **WebMD**, one of the largest online health information platforms and a major channel for pharmaceutical advertising aimed at healthcare professionals. WebMD runs campaigns across many tactic types, client segments, and physician specialties, and planning those campaigns well depends on knowing how they are likely to perform before the budget is committed.

The objective is to use campaign data from January through June to forecast key second half metrics: total spend, cost per engagement, and engagement volume. Accurate forecasts help media planners allocate budget toward tactics and audiences that deliver engagement efficiently, and help set realistic expectations with pharmaceutical clients. The interpretability side matters as much as the accuracy. Knowing *which* combinations of specialty, tactic, and geography move CPE gives the business something it can act on, not just a number.

**Timeline**

| Month | Focus |
|-------|-------|
| September | Data cleaning, exploratory data analysis, data quality audit, produce a cleaned dataset |
| October | Feature engineering, baseline and tree based models, performance comparison |
| November | Hyperparameter tuning, final evaluation, presentation deck, business recommendations |

---

## 📊 **Data Exploration**

*In progress. This section will cover:*

* The WebMD campaign dataset: origin, format, size, and the fields describing tactic type, client segment, healthcare professional specialty, geography, spend, and engagement
* Cleaning and preprocessing steps, including how missing and inconsistent records were handled
* Findings from exploratory data analysis, such as spend and engagement distributions, seasonality between H1 and H2, and differences across specialties and tactics
* Data quality issues found during the audit, and the assumptions made when working around them

**Planned visualizations:** spend and CPE distributions, engagement by specialty and tactic, correlation heatmap, time series of monthly campaign volume.

---

## 🧠 **Model Development**

*In progress. Planned approach:*

* **Baseline:** linear and regularized regression models to establish a reference point for each target metric
* **Primary models:** tree based regressors, including random forest and XGBoost, chosen for their handling of mixed categorical and numerical campaign features
* **Targets:** total spend, cost per engagement, and engagement volume, modeled separately with multi output regression explored as a stretch goal
* **Feature engineering:** encoding of tactic type, client segment, and specialty, geography level aggregates, and H1 derived rate features
* **Training setup:** H1 data for training and validation, held out H2 data as the test set, with MAPE and R² as the primary evaluation metrics

---

## 📈 **Results & Key Findings**

*To be completed after model evaluation.* This section will report:

* MAPE and R² for each target metric against the H2 test set, measured against the MAPE below 30 percent and R² above 0.55 targets
* How the tree based models compare to the regression baseline
* The campaign characteristics most associated with high and low CPE
* Fairness and consistency of performance across client segments and specialties, so no group of campaigns is systematically mispredicted

**Planned visualizations:** predicted versus actual plots, residual distributions, feature importance rankings, SHAP summary plots.

---

## 🚀 **Next Steps**

Stretch goals and open directions for the project:

* **Multi output regression** to predict spend, CPE, and engagement jointly rather than in separate models
* **Clustering pipelines** to group campaigns by behavior profile before modeling
* **Time series ensembles** to capture seasonality that a flat H1 to H2 split may miss
* **SHAP interpretability analysis** to explain individual predictions to media planning stakeholders
* **A data quality flagging dashboard** that surfaces suspect records before they reach the model

Known limitations and what we would explore with more time or data will be documented here as the work progresses.

---

## 📝 **License**

*To be selected with approval from our Challenge Advisor.*

---

## 📄 **References**

* scikit-learn documentation, preprocessing and regression modules
* XGBoost documentation
* pandas documentation
* SHAP documentation

---

## 🙏 **Acknowledgements**

Thank you to **WebMD** for hosting this challenge project and providing the campaign data, to our Challenge Advisor **Kimia Naeiji** for the biweekly guidance, and to our AI Studio Coach **Anushka Naik**. Thank you also to the **Break Through Tech AI Program** team for making this studio possible.ents** (Optional but encouraged)

Thank your Challenge Advisor, host company representatives, TA, and others who supported your project.
