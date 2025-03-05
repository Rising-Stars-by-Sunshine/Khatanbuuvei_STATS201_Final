# README.md - Documentation

## Code Execution

To run the code for this project, you can use the provided Google Colab notebooks. These notebooks are pre-configured to work directly with your dataset and include the necessary code for data analysis, modeling, and visualizations.

### Step-by-Step Instructions:

1. **Open Google Colab Notebook**:  
   Click on one of the following links to open the Google Colab notebooks:
   
   - [Notebook 1: Simulation and Analysis](https://colab.research.google.com/drive/1oVziIK3-KXwJaWqfeIZNxvMg2UFbZk3I?usp=sharing)
   - [Notebook 2: Regression Discontinuity Analysis](https://colab.research.google.com/drive/1BYankPDZ6_INgdxm51co9IM_xgLTu5-H?usp=sharing)

2. **Connect to Google Drive**:  
   If prompted, connect the notebook to your Google Drive so you can upload and download necessary files like datasets.

3. **Import Dataset**:  
   Use the provided links or your Google Drive to upload the necessary datasets. Once the dataset is uploaded, load it into the environment using Pandas:
   
   ```python
   import pandas as pd
   data = pd.read_csv('DIS_stock_price.csv')
   ```

4. **Run the Code**:  
   Follow the cells in the notebook. Each section of code will be clearly labeled, so you can run the analysis step-by-step.

### Colab Setup:
- Open the notebook using the provided link.
- Ensure that the required datasets are available in the environment.
- Execute each code block to analyze the data, build models, and visualize results.

---

## Dependencies

To successfully run the code, you'll need to install the following libraries. You can install these libraries using `pip` or by adding them to a `requirements.txt` file for easy installation.

### Required Libraries:
```bash
# Install required libraries:
pip install pandas==1.5.0
pip install numpy==1.23.0
pip install matplotlib==3.5.2
pip install seaborn==0.11.2
pip install scikit-learn==1.1.1
pip install statsmodels==0.13.0
```

### Required Libraries:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.ensemble import RandomForestRegressor
from sklearn.metrics import mean_absolute_error, mean_squared_error
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LinearRegression
import statsmodels.api as sm
from statsmodels.formula.api import ols
```

Make sure to use compatible versions of these libraries for the project to work correctly. If you're using Google Colab, the environment should have most of these libraries pre-installed.

---

## Example Usage

Here’s an example of how to use the code to run an analysis on the dataset.

### 1. **Data Preprocessing:**

Start by loading the dataset and performing any necessary data cleaning steps.

```python
data = pd.read_csv('DIS_stock_price.csv')

print(data.head())

# Handle any missing values
data.fillna(method='ffill', inplace=True)
```

### 2. **Building a Model (e.g., Random Forest Regressor):**

Here’s how to use a machine learning model like Random Forest to predict subscriber growth based on content strategies and pricing:
```python
# Define the features and target
X = data[['price', 'content_type', 'genre']]
y = data['subscribers']

# Split the data into training and test sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Initialize the RandomForest model
model = RandomForestRegressor(n_estimators=100, random_state=42)

# Fit the model
model.fit(X_train, y_train)

# Predict on the test set
y_pred = model.predict(X_test)

# Evaluate the model
mae = mean_absolute_error(y_test, y_pred)
mse = mean_squared_error(y_test, y_pred)

print(f"Mean Absolute Error: {mae}")
print(f"Mean Squared Error: {mse}")
```

### 3. **Visualization:**

You can visualize the relationship between features and predictions using seaborn or matplotlib:
```python
# Plot feature importances
feature_importances = model.feature_importances_
plt.barh(X.columns, feature_importances)
plt.xlabel('Feature Importance')
plt.title('Feature Importance for Subscriber Growth Prediction')
plt.show()
```
