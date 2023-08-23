# Big-Mart-Sales-Prediction
## Task:
Build a Machine Learning Model to Predict Big Mart Sales. We have been provided with a labelled dataset, so this will come under **Supervised Learning**.</br>
As we have to predict continuous values i.e. sales we used Regression Techniques for this. 3 different types of Regression models are used here: XGBRegressor, Random Forest Regressor and Linear Regressor
## Dataset:
The dataset is being taken from Kaggle's **BigMart Sales Data**. The dataset contains 8523 records and 12 features. The features are:</br>
- Item_Identifier</br>
- Item_Weight      </br>          
- Item_Fat_Content   </br>         
- Item_Visibility    </br>        
- Item_Type</br>                 
- Item_MRP </br>                  
- Outlet_Identifier  </br>        
- Outlet_Establishment_Year </br> 
- Outlet_Size      </br>          
- Outlet_Location_Type </br>      
- Outlet_Type        </br>        
- Item_Outlet_Sales </br></br>

link: https://www.kaggle.com/datasets/brijbhushannanda1979/bigmart-sales-data?select=Train.csv


## Steps Involved:
### Import Dependencies
Libraries needed for the task are:</br>
- numpy</br>
- pandas</br>
- seaborn</br>
- train_test_split from sklearn.model_selection</br>
- Linear Regression from sklearn.linear_model</br>
- metrics from sklearn</br>
- Label Encoder from sklearn.preprocessing</br>
- Random Forest Regressor from sklearn.ensemble</br>
- XGB Regressor from XGBoost
### Data Collection 
Use the read_csv function of pandas to import the dataset.</br>
shape, head, describe and isnull() functions can be used to know our dataset.</br>
### Data Processing
1. Handling the missing value:</br>
   Replaced the NaN values of 'Item-weight' with the mean of the column. </br>
   Replaced null values of Outlet_Size with the mode value of Corresponding Outlet_Type</br>
3. Data Cleaning: Replace the similar value with the same style</br>
4. Label Encoding: Convert all the categorical text data to respective numerical values using the LabelEncoder class.</br>

Finally, Split the dataset into features(X) and target(Y) using the **drop** function, such as the target contains only the Class column which depicts the item sales. The feature contains all the rest of the columns.</br>
### Split into train and test
In this, we had split the dataset into 4 parts x train, x test, y train and y test where y contains all the label data whereas x contains the features dataset.</br>
We have taken 10% of the data for training while the remaining 90% is kept for training purposes.</br>
### Model Training and Evaluation</br>
1. **XGBoost Regressor**:</br>
R2 Square score for trained Data: 0.9375418436087201</br>
R2 Square score for test Data: 0.5674497228540715</br>
2. **Random Forest Regressor**:</br>
R2 Square score for trained Data: 0.9375418436087201</br>
R2 Square score for test Data: 0.5674497228540715</br>
3. **Linear Regression**:</br>
R2 Square score for trained Data: 0.5030274397300731</br>
R2 Square score for test Data: 0.5080317759616186</br>

</br></br></br>

Reference: Project 12. Big Mart Sales Prediction using Machine Learning with Python | Machine Learning Projects, Siddhardhan, https://www.youtube.com/watch?v=epI9W3MZ3Ts&list=PLfFghEzKVmjvuSA67LszN1dZ-Dd_pkus6&index=13

