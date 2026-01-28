<H3>NAME: VESHWANTH.</H3>
<H3>REG NO:212224230300</H3>
<H3>EX. NO.1</H3>
<H3>DATE: 28-01-2026</H3>
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
## Importing all Libraries:
    import pandas as pd 
    from sklearn.preprocessing import MinMaxScaler,LabelEncoder 
    from sklearn.model_selection import train_test_split 
    from scipy import stats 
    import matplotlib as plt

## Importing the Dataset:
    df=pd.read_csv("C:\\Users\\admin\\Pictures\\Churn_Modelling.csv")
    df

## Displaying Null and Duplicated values:
    df.isnull().sum()

    df.duplicated
## Displaying columns:

    df.columns
## Using heads and tail to display the data:

    df.head(5)
    df.tail(5) 

## Assigning Y values:
    y = df.iloc[:, -1].values
    print(y)

##  Describing Dataset:
    df.describe

## Removing a part of columns:
    data = df.drop(['Surname', 'Geography','Gender'], axis=1)
    data.head()
 ## Normalizing a Dataset:
    scaler=MinMaxScaler()
    df1=pd.DataFrame(scaler.fit_transform(data))
    df1
## Assigning X and Y values:
    X=df.iloc[:,:-1].values
    y=df.iloc[:,-1].values
    print(X)
    print(y)
## Using train_test_split to split dataset:
      X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
      print("X_train\n")
      print(X_train)
      print("\nLenght of X_train ",len(X_train))
      print("\nX_test\n")
      print(X_test)
      print("\nLenght of X_test ",len(X_test))
## OUTPUT:
## Importing the Dataset:

<img width="1667" height="946" alt="image" src="https://github.com/user-attachments/assets/8f13f099-de5e-4124-b9d5-619ee6775cd7" />

 ## Using heads and tail to display the data:
 <img width="1595" height="599" alt="image" src="https://github.com/user-attachments/assets/46be53a7-4116-4d80-b0df-a93be77a5918" />

 ## Displaying columns:
 <img width="1398" height="145" alt="image" src="https://github.com/user-attachments/assets/ffebac71-3a87-4f53-bf79-2769030bae4e" />

## Displaying Null and Duplicated values:
<img width="1231" height="354" alt="image" src="https://github.com/user-attachments/assets/68620646-3283-4979-8061-56629ad80331" />
<img width="1405" height="709" alt="image" src="https://github.com/user-attachments/assets/9693708d-fdbc-47d0-a2b6-51d88812c5ff" />
<img width="1392" height="393" alt="image" src="https://github.com/user-attachments/assets/f3e16b36-837a-4f16-bad3-8e01de74397f" />

## Assigning Y values:
<img width="1429" height="98" alt="image" src="https://github.com/user-attachments/assets/e481955b-394f-4c52-b32f-b3667ad45b2c" />

##  Describing Dataset:
<img width="1434" height="760" alt="image" src="https://github.com/user-attachments/assets/72c1e54d-08de-4989-b143-350414e8ba9a" />
<img width="1426" height="376" alt="image" src="https://github.com/user-attachments/assets/afddb5e5-81d5-4d6d-a8d2-839fa850341b" />

## Removing a part of columns:
<img width="1441" height="342" alt="image" src="https://github.com/user-attachments/assets/88ac9ff5-ac99-46a1-be1c-036b5b61a593" />

 ## Normalizing a Dataset:
 <img width="1411" height="528" alt="image" src="https://github.com/user-attachments/assets/67a615ce-b031-4ce4-94cd-1503ee61ab7b" />


 ## Assigning X and Y values:
 <img width="1391" height="305" alt="image" src="https://github.com/user-attachments/assets/5afd22d8-fb32-4378-b2a0-9113a8d67061" />

 ## Using train_test_split to split dataset:
 <img width="1379" height="685" alt="image" src="https://github.com/user-attachments/assets/8486eff6-e4ec-4411-b882-eb3a40e36cb6" />



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


