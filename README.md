# Task_3
The main objective of this task is to perform exploratory data analysis (EDA), data preprocessing, and model training using a decision tree classifier on a bank dataset. The dataset is used to predict whether a client will subscribe to a term deposit.

**Procedures**
**Importing Libraries and Data:**
Essential libraries such as pandas, numpy, matplotlib.pyplot, seaborn, and sklearn are imported.
The dataset is read from a CSV file and stored in a DataFrame called datas.
The column 'y' is renamed to 'deposit' for clarity.

**Initial Data Inspection:**
The head, tail, shape, column names, data types, and basic information about the DataFrame are displayed.
The number of duplicated rows and missing values in the DataFrame is checked.

**Identifying Categorical and Numerical Columns:**
Columns with object data types are identified as categorical columns (cat_cols).
Columns with non-object data types are identified as numerical columns (num_cols).

**Descriptive Statistics:**
Descriptive statistics for numerical columns are displayed using datas.describe().
Descriptive statistics for categorical columns are displayed using datas.describe(include='object').

**Data Visualization:**
Histograms for numerical features are plotted to understand their distributions.
Bar plots for categorical features are created to show the frequency of each category.
Box plots for all features are plotted to visualize the spread and identify potential outliers.

**Outlier Detection and Removal:**
For selected numerical columns (age, campaign, duration), outliers are detected and removed using the IQR (Interquartile Range) method.

**Correlation Analysis:**
A correlation matrix for numerical columns is computed and printed.
A heatmap is plotted to visualize the correlation matrix, highlighting correlations above a threshold of 0.90.
Columns with high correlation ('emp.var.rate', 'euribor3m', 'nr.employed') are identified and dropped from the DataFrame.

**Label Encoding:**
Categorical variables are encoded into numerical values using LabelEncoder from sklearn.

**Splitting Data:**
The dataset is split into training and testing sets with a 75-25% ratio using train_test_split.

**Model Training and Evaluation:**

Two decision tree classifiers are trained using different criteria **(Gini impurity and entropy) and hyperparameters**.
The models are evaluated using training and testing scores.
Predictions are made on the test set, and performance metrics (accuracy, confusion matrix, classification report) are computed.
The decision trees are visualized using plot_tree.

