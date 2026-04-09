## Loan Pricing Decisioning Engine

### System Overview
This project implements a prescriptive analytics system that determines optimal car loan interest rates by explicitly optimizing expected revenue, rather than predicting acceptance alone.

The system separates probability modeling from decision logic, reflecting how ML models are used in real pricing and policy engines.

---

### Pipeline
1. Data cleaning and outlier handling
2. Feature engineering for acceptance and revenue modeling
3. Model training and comparison (XGBoost, Random Forest, SVM, KNN, Logistic Regression)
4. Cross-validation and hyperparameter tuning
5. Pricing policy optimization over interest rate permutations

---

### Objective Function
Expected Revenue is defined as:

Expected Revenue = P(Acceptance) × Interest Rate × Loan Amount

The optimized system selects the interest rate that maximizes this value for each customer profile.

---

### Evaluation
- Fixed train / validation / test splits
- Cross-validation with GridSearchCV
- Model comparison under identical preprocessing
- Final XGBoost validation accuracy: 94.1%

---

### Key Insight
Increasing interest rates improves profit per accepted loan but reduces acceptance probability.  
Expected revenue peaks at a non-obvious interior optimum, not at extreme pricing.

---

### Outcome
Applying the optimized pricing policy resulted in a 79% projected increase in expected revenue compared to baseline quoted rates.

---

### Production Notes
- Pricing logic is decoupled from model training
- Policy can be re-evaluated as models retrain
- Suitable for A/B testing and monitoring in deployment
