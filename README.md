# Bangalore-House-Prediction

This model predicts the price of Bangalore's house with the help of a few parameters like availability, size, total square feet, bath, location, etc.

areas covered:
Exploratory data analysis
Dealing with a missing values or noisy data
Data preprocessing
Create new features from existing features
Remove outliers
Data visualisation
Splitting data into the training and testing 
Train linear regression model and test.

FIND BEST MODEL USING GRIDSEARCHCV:-
linear regression comes out to be the best approach with accuracy around 84.01 
	
We perform an Exploratory Data Analysis. In EDA, drop some features (columns) which are of no use to train our model. 
Then remove the outliers from the BHK. firstly check the BHK greater than 22. If it’s greater than 22 which means it’s outlier.
Further we create a user defined function is_float()  with the the total_sqft as an argument and return all the floating (function convert integer values into float).
describe a price_per_sqft feature and in this, you can see the outlier. House price is 176470 Lakh which is not possible according to location and total square feet. So create a function remove_outlier_from_price_per_sqft(). It takes a dataset and uses a Standard Deviation technique to remove outliers.
Next then we apply a one hot encoding to convert a categorical feature into numeric feature. And store into a “dummies” data set.
Now concate dummies data set with our final data set and remove a “other” column from “dummies” data set. 
Test the model using the testing data set and after testing you can see our model predicts below values and you can also see the actual values. 

Changes for better accuracy: Under Dimensionality Reduction 

ANY LOCATION HAVING LESS THAN 12 DATA PINTS WILL BE TAGGED AS "OTHER" LOCATION. THIS WAY NUMBER OF CATEGORIES WERE REDUCED BY HUGE AMOUNT. LATER ON WHEN WE DO ONE HOT ENCODING, IT WILL HELP US WITH HAVING FEWER DUMMY COLUMNS.
