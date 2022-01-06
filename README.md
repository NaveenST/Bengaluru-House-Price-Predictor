# Bengaluru-House-Price-Predictor
Machine Learning Project to predict house prices in Bengaluru City.

# Introduction-

This project deals with predicting house prices in Bengaluru City using various factors such as area type, location, area sqft, bedrooms, bath & balcony. Buying a house or plot is a life long commitment and should not be encountered without sufficient information about the house, dimensions and market value/selling price. This project is an attempt to predict the house prices in an efficient way by considering real world factors which influence the prices.

# Data-

The dataset consists of around 13,000 records along with the sufficient attributes to describe it-
1) area type - describes the type of the property such as empty plot or built-up area or super built-up area and so on.
2) availability - describes the plot/house availability. (usually it is a date with month or sometimes speaks about the vacany for immediate move-in).
3) location - describes the location of the house. One of the major factor that influence's the house price.
4) size - consists info about the house. (usually something like 2BHK/3BHK and so on).
5) society - describes the locality of the house/plot.
6) total sqft - provides information about the total area of the house/plot in square feet.
7) bath - contains the info the number of bath rooms in the house.
8) balcony - describes whether the house contains any patio/veranda.
9) price - contains the selling price of the house/plot.

# Data Cleaning and Analysis- 

The dataset contains a single csv file of about 13,000 records. And consists of 9 columns (6 object type and 3 numeric type), each describing the attributes of a single house/plot. The initial stages of any data cleaning process consists of checking the null values, shape, data type and data itself. After that we need to analyse the total counts for each values within a column and for entire dataset as well. The main objective of data cleaning for this project is wrt to model training, hence the data cleaning tries take a path where it assists the model building process by setting up the raw data into model compatible one.
The distribution of the values plays an essential role in identifying any outliers within the data and combined with business domain knowledge, we should be able to get a pure data with high value which makes any model built on top of it a highly efficient one.

1) In order to fill the null values we have tackled issue for categorical and numerical fields separately. For categorical, we have show the distribution of all the values along with the nulls and made a calculated assumption as to what kind of values would have been inserted for this nulls. And for numerical, we have compared mean and median values, before plugging in the suitable values through business knowledge lens.

  Categorical field -
  
  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/896e14360640766813cf5633ed733ca6677f5be6/Screenshots/Null%20values%20Distribution%20for%20Balcony.png)


  Numerical field -
  
  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/896e14360640766813cf5633ed733ca6677f5be6/Screenshots/Null%20values%20Distribution%20for%20bath%20rooms.png)
  
2) Distribution of values for various fields-

Bath rooms-

  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/1c203982de530a9e70523b21a6f80c980c389d6b/Screenshots/Distribution%20of%20Bath%20rooms.png)
  
Price per sqft-

  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/1c203982de530a9e70523b21a6f80c980c389d6b/Screenshots/Price%20per%20sqft%20distribution.png)
  
  
3) Total sqft v/s Price before outliers removal-

Rajajinagar-

  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/1c203982de530a9e70523b21a6f80c980c389d6b/Screenshots/Rajajinagar%20total_sqft%20vs%20price.png)
  
Hebbal-

  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/1c203982de530a9e70523b21a6f80c980c389d6b/Screenshots/Hebbal%20total_sqft%20vs%20price.png)
  
After removal of outliers-

Rajajinagar-

  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/1c203982de530a9e70523b21a6f80c980c389d6b/Screenshots/Rajajinagar%20total_sqft%20vs%20price(After%20removing%20outliers).png)
  
Hebbal-

  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/1c203982de530a9e70523b21a6f80c980c389d6b/Screenshots/Hebbal%20total_sqft%20vs%20price(After%20removing%20outliers).png)
  
  
Comparison before/after removal of outliers-

Rajajinagar-

  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/219aeeb6f6650bd20da0e4ca0b327fadbc60c3c6/Screenshots/Rajajinagar%20compare.png)
  
  
Hebbal-

  ![image](https://github.com/NaveenST/Bengaluru-House-Price-Predictor/blob/219aeeb6f6650bd20da0e4ca0b327fadbc60c3c6/Screenshots/Hebbal%20compare.png)



