Ames Housing Price Predictor (92.5% R²)
Executive Summary
This project delivers a high-performance regression model to predict residential home prices in Ames, Iowa. By moving beyond basic linear regression to Lasso Regularization and performing rigorous feature engineering, the model achieves a Mean Absolute Error (MAE) of ~$15,270, representing a significant improvement over baseline models.

🛠️ The Workflow (What I Did)
Unlike standard tutorials, this project followed a strict Data Science lifecycle to ensure model reliability:

Advanced Data Cleaning: Identified and removed 3 critical outliers (high square footage but low price) that were skewing the mathematical "logic" of the model.

Feature Engineering: Engineered "Power Features" including Total_SF (summing basement and floor areas) and House_Age to provide better context than raw year data.

Categorical Consolidation: Handled "Noise" in text data by grouping rare categories (e.g., infrequent roof materials) into an Other bucket to prevent model overfitting.

Language Translation (Encoding): Utilized One-Hot Encoding to convert 70+ categorical labels into 250+ numerical "switches" for the AI to process.

Lasso Regularization: Implemented Lasso (L1) regression to automatically perform feature selection, effectively "silencing" 0.3-correlation noise and focusing on high-impact variables.

Results & Insights
Top Predictors: The model correctly identified Gr Liv Area, Total_SF, and Overall Quality as the most influential price drivers.

Residual Analysis: Evaluated model "blunders" to identify Heteroscedasticity in the luxury home segment (>$500k), acknowledging the impact of low sample size on high-end predictions.

📁 Project Structure
data/ : Original Ames dataset.

notebooks/ : The complete 27-cell end-to-end pipeline (Cleaning, EDA, Modeling).

requirements.txt : Python dependencies (Pandas, Scikit-Learn, Seaborn).

🚀 How to Run
Clone the repo: git clone <your-url>

Create virtual environment: python -m venv venv

Install dependencies: pip install -r requirements.txt

Run the Jupyter Notebook in notebooks/.
