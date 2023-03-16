# FAO-Crop-Analysis-ML

## Data Preprocessing:
- We acquired the data from the FAO and World Data Bank website
mentioned in the documentation.
- From the FAO website we got Area Harvested (Feature), Production
(Feature) and Yield (Target) data.
- From the World Data Bank website we got Precipitation, Minimum
Temperature, Maximum temperature and Mean Temperature data
(Features).
- The data acquired is for a single country (in our case India) from the
year 1961 to 2020.
- We merged the two datasets acquired into one single dataset using
the common Year column.
- We encoded the Item Code Column / Feature.
- We removed the unwanted and redundant columns from the data set
according to feature importance.
- We then check for non-null values in each column so that those values
could be trimmed off. We find that there is no null value in any column.
- We use two datasets in this work:
  - Dataset with All the crops in FAO website
  - Dataset with only One crop (banana) in FAO website
- Data Analysis is done and explained in the code below clearly.

## Relationship between features:
The features in consideration were production, area harvested, item code,
precipitation, minimum temperature, maximum temperature and mean
temperature . We examined the relationship between features using the
correlation matrix and plotted a heatmap for the same. Production feature had
the highest correlation with yield.In terms of correlation among features minimum
,maximum and mean temperatures were highly correlated with value > 0.5 ,so we
chose the feature minimum temperature which had higher correlation with the
output variable yield and dropped the features maximum and average
temperatures. We also dropped the feature year as we didn’t find much
correlation to the output yield.
We included the feature item code which helped identify different crops as they
require different rainfall and minimum temperature which affect the yield.
Therefore item code becomes an important feature to predict the yield for a
particular crop type.

## Training and Testing Dataset:
Divided the data into training and testing where 67% of data was used for
training and the remaining 33% was kept for testing.
### Evaluation Metrics:
The Problem presented is a Regression Problem as the Target variable
(Yield) is Continuous. So we use these following evaluation metrics.
We have used R 2 score and MSE to evaluate the different models.
- R 2 Score - The R 2 score varies between 0 and 100%. It is closely related to the
MSE. It is (total variance explained by model) / total variance. So if it is 100%, the
two variables are perfectly correlated, i.e., with no variance at all. A low value
would show a low level of correlation, meaning a regression model that is not
valid, but not in all cases.
- MSE - Mean square error (MSE) is the average of the square of the errors. The
larger the number the larger the error. Error in this case means the difference
between the observed values y1, y2, y3, … and the predicted ones pred(y1),
pred(y2), pred(y3), … We square each difference (pred(yn) – yn)) ** 2.
Heatmap - Heatmap visualization or heatmap data visualization is a method of
graphically representing numerical data where the value of each data point is
indicated using colors.
