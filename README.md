# Prediction of Product Sales.
## This first project will be a sales prediction for food items sold at various stores.

Zalwango Diana

Many retail outlets usually have a number of items on sale that are suitably prepared for the consumers in those same areas where the outlets are located. These items could range in price, quality, brand and quantity. Thus we can see that sales made rely on the choices that custometrs make.
## Data Source:
Prediction of  Product Sales : https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

For this dataset, there were 8523 rows and 12 columns.
## Data Dictionary
![dd-predictions](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/617a5261-1af1-46c4-a696-f821aa894538)

## To prepare this data,the data was cleaned  and the following processes were performed:
The task was to create exploratory visuals that might help you understand, explain, or model your data. This must included at least one of each:
Histograms to view the distributions of numerical features in your dataset.
Boxplots to view statistical summaries of numerical features in your dataset.
Countplots to view the frequency of each class of categorial features in your dataset.
Heatmap to view the correlation between features.
I have selected key visuals of different types that demonstrate a relevant insight into the data

![EDA for Item_Visibility](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/4f60ddc9-6bdc-42a4-adf8-1482ee107b93)
- The barplot seems to have a big number of items with low visibility percentage whose count is below 200.
- We are having many outliers from this column. These could be items that are highly given display space or marginalized with low percentages of visibility compared to other items. The items above the median percentage of visibility can bring in more sales compared to those below the median percentage of visibility.

![EDA for Outlet_Sales](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/9f14e894-d905-46a4-9fcd-b58ca7cf9c47)
- There are less item outlet sales that are above the median sales,this shows that they are for the items most sought after.

- The sales above median are consistently high compared to those below median which keep reducing.

![Barplot for Item_Type](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/2a0216bc-30a0-431d-b3ee-00c03bb40048)
- Fruits and vegetables, snacks and household items are the leading items in sales while seafoods and breakfast are preferred by less numbers of people.

![Correlation for Numeric_features](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/8ea3afd2-d52b-4fe2-8dab-421fe6ae1c45)
- There is moderate positive correlation of 0.57 between Item MRP and the Item Outlet sales,showing that as as prices of items increase, the higher the sales generated.
- There is a negative correlation between Item visibility and Outlet year of establishment of -0.07 showing that as the visibility of the item decreases,the Year of Establishment of the outlet shows to be earlier. This also shows that older outlets might have lower percentages of visibility of the Items.

Maching Learning Using the Following Models:
 - Linear Regression Model
 - Random Forest Regressor Model
 - Tuned Random Forest Regressor Model

# Models Evaluated and Results.
- Linear Regression Model(testing set):
  - MAE = 804.622
  - MSE = 1,195,459.654
  - RMSE = 1,093.371
  - R^2 = 0.567
    
- Random Forest Regressor Model (Testing Set):
   - MAE = 766.353
   - MSE = 1,216,710.913
   - RMSE = 1,103.046
   - R^2 = 0.559

 -Tuned Random Forest Regressor Model (Testing Set):
   - MAE = 739.275
   - MSE = 1,130,745.938
   - RMSE = 1,063.365
   - R^2 = 0.590

- The Final Model Chosen was the Tuned Random Forest Regressor Model with the n_estimators tuned to 200.

- For the testing set on the model, 59.0% of the variance in y was explained by x.

- The Mean Absolute Error was off by about 739.275.

 - The Mean Squared Error was 1,130,745.938 .

-  The Root Mean Squared Error had a calculation of 1,063.365.

