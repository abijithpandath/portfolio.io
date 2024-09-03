# Essential Python Programs for Data Scientists


## 1. Read and Display a CSV File
```python
import pandas as pd

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Display the first few rows
print(df.head())
```


## 2. Basic Data Cleaning (Handling Missing Values)
import pandas as pd
```python
# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Fill missing values with the mean of the column
df.fillna(df.mean(), inplace=True)

# Display the cleaned data
print(df.head())
```

## 3. Descriptive Statistics
```python
import pandas as pd

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Get descriptive statistics
print(df.describe())
```

## 4. Data Visualization (Histogram)
```python
import pandas as pd
import matplotlib.pyplot as plt

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Plot histogram
df['column_name'].hist()
plt.xlabel('Value')
plt.ylabel('Frequency')
plt.title('Histogram of Column')
plt.show()
```

## 5. Correlation Matrix
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Calculate correlation matrix
corr = df.corr()

# Plot heatmap
sns.heatmap(corr, annot=True, cmap='coolwarm')
plt.title('Correlation Matrix')
plt.show()
```

## 6. 6. Train-Test Split
```python
from sklearn.model_selection import train_test_split
import pandas as pd

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Define features and target
X = df.drop('target', axis=1)
y = df['target']

# Split data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

print(X_train.shape, X_test.shape)
```

## 7. Simple Linear Regression
```python
from sklearn.linear_model import LinearRegression
import pandas as pd

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Define features and target
X = df[['feature']]
y = df['target']

# Initialize and train model
model = LinearRegression()
model.fit(X, y)

# Make predictions
predictions = model.predict(X)
print(predictions)
```

## 8. K-Means Clustering
```python
from sklearn.cluster import KMeans
import pandas as pd

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Define features
X = df[['feature1', 'feature2']]

# Initialize and fit K-Means model
kmeans = KMeans(n_clusters=3)
kmeans.fit(X)

# Get cluster centers and labels
centers = kmeans.cluster_centers_
labels = kmeans.labels_

print('Cluster Centers:', centers)
print('Labels:', labels)
```

## 9. Decision Tree Classifier
```python
from sklearn.tree import DecisionTreeClassifier
import pandas as pd

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Define features and target
X = df.drop('target', axis=1)
y = df['target']

# Initialize and train model
model = DecisionTreeClassifier()
model.fit(X, y)

# Make predictions
predictions = model.predict(X)
print(predictions)
```

## 10. Cross-Validation
```python
from sklearn.model_selection import cross_val_score
from sklearn.linear_model import LogisticRegression
import pandas as pd

# Read CSV file using a relative path
df = pd.read_csv('paste your relative path')

# Define features and target
X = df.drop('target', axis=1)
y = df['target']

# Initialize model
model = LogisticRegression()

# Perform cross-validation
scores = cross_val_score(model, X, y, cv=5)

print('Cross-Validation Scores:', scores)
print('Average Score:', scores.mean())
```
