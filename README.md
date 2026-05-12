<H3>ENTER YOUR NAME: LIGNESHWAR K</H3>
<H3>ENTER YOUR REGISTER NO. 212223230113</H3>
<H3>EX. NO.1</H3>
<H3>DATE 12-00-2026</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
TYPE YOUR CODE HERE
```python
#import libraries
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

#Read the dataset from drive
df = pd. read_csv( '/content/Churn_Modelling.csv' )
print(df)

#split the dataset
X = df. iloc[ :, : -1] . values
print (X)
y = df . iloc[ :, -1] . values
print(y)

# Finding Missing Values
print(df.isnull().sum())

#Handling Missing values
print(df.isnull() .sum() )
y = df . iloc[ :, -1] . values
print(y)

#Check for Duplicates
df.duplicated()

#Detect Outliers
scaler = MinMaxScaler()

# Select only numerical columns for scaling
numerical_cols = df.select_dtypes(include=['number'])
df1 = pd.DataFrame(scaler.fit_transform(numerical_cols))
print(df1)

#splitting the data for training & Testing
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2)

#'test_size=0.2' means 20% test data and 80% train data
print(X_train)
print(len(X_train))
print(X_test)
print(len(X_test))
```

## OUTPUT:
### Read the dataset
<img width="874" height="834" alt="image" src="https://github.com/user-attachments/assets/b232e551-4484-408f-8258-c7a577a375ac" />

### split the dataset
<img width="774" height="223" alt="image" src="https://github.com/user-attachments/assets/53b25fe5-d890-4810-8ed4-751e2fcfe2ac" />

### Finding Missing Values
<img width="667" height="328" alt="image" src="https://github.com/user-attachments/assets/bd4de803-abab-41d6-89d3-f747a59f33a5" />

### Handling Missing values
<img width="728" height="345" alt="image" src="https://github.com/user-attachments/assets/a20db9ed-f969-45d2-bbe5-bcd5b825ef85" />

### Check for Duplicates
<img width="617" height="272" alt="image" src="https://github.com/user-attachments/assets/146f93ae-30fd-465c-ac40-cc360f47931a" />

### Normalized dataset
<img width="994" height="557" alt="image" src="https://github.com/user-attachments/assets/ae1dcad9-4fbc-49ed-884f-117f14dc5b8b" />

### Print train and test data
<img width="765" height="352" alt="image" src="https://github.com/user-attachments/assets/a0fe9ec4-78ae-4c43-b2cf-5cd2045b0681" />



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


