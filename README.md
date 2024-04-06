![320211331-8b824608-682e-4591-a318-368fc9817339](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/54be62ac-1a92-4713-b620-269b829a6abc)

# Prediction of Product Sales.
## This project will be a sales prediction for food items sold at various stores.

Zalwango Diana

## Overview of the Project.
In this project, we aimed to predict BigMart sales using machine learning techniques. Many retail outlets usually have a number of items on sale that are suitably prepared for the consumers in those same areas where the outlets are located. These items could range in price, quality, brand and quantity. Thus we can see that sales made rely on the choices that customers make. Our goal was to build a robust model that accurately predicts sales based on relevant features.

## Data Source:
Prediction of  Product Sales : https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

For this dataset, there were 8523 rows and 12 columns.
## Data Dictionary
![dd-predictions](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/617a5261-1af1-46c4-a696-f821aa894538)

## To prepare this data,the data was cleaned  and the following processes were performed:
During the explaratory data analysis:
- Histograms were visualized to view the distributions of numerical features.
- Boxplots were visualized to view statistical summaries of numerical features.
- Countplots were visualized to view the frequency of each class of categorial features.
- A Heatmap was visualized to view the correlation between features.
I have selected key visuals of different types that demonstrate a relevant insight into the data.

![Item_Fat_Content](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/4c924c5c-9156-4c62-80b0-c4403620bca0)

- The count plot shows  a higher frequency for items with low fat.
- This feature can be a predictor of our target because the customers would buy more items with desired fat content depending on their age,health situations and tastes.

![Item_MRP](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/4b2a2742-8172-4fd7-868b-363a310270cf)

- This feature is vital for both sellers and consumers in their decision making about the various items in the outlets.

- Most item prices range between 100 to 200. 

![Barplot for Item_Type](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/2a0216bc-30a0-431d-b3ee-00c03bb40048)
- Fruits and vegetables, snacks and household items are the leading items in sales while seafoods and breakfast are preferred by less numbers of people.

![Correlation for Numeric_features](https://github.com/zal-developer/Production-of-Product-Sales./assets/119515838/8ea3afd2-d52b-4fe2-8dab-421fe6ae1c45)
- There is moderate positive correlation of 0.57 between Item MRP and the Item Outlet sales,showing that as as prices of items increase, the higher the sales generated.
- There is a negative correlation between Item visibility and Outlet year of establishment of -0.07 showing that as the visibility of the item decreases,the Year of Establishment of the outlet shows to be earlier. This also shows that older outlets might have lower percentages of visibility of the Items.

## Relevant Insights from the Data

- Impact of Item Fat Content on Sales:
  
We observed that items with low fat content tend to have higher sales. This insight suggests that fat content plays a crucial role in sales performance.

Visualization: A bar chart comparing average sales across regular and low fat content in items is included.


- Product Type Influence on Sales:
  
Certain product types consistently contribute more to overall sales. For instance, perishable items or high-demand products may have a significant impact.

Visualization: A barplot showing the distribution of sales by product type is included.

## Machine Learning Using the Following Models:
 - Linear Regression Model
 - Random Forest Regressor Model
 - Tuned Random Forest Regressor Model

## Models Evaluated and Results.
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

 - Tuned Random Forest Regressor Model (Testing Set):
   - MAE = 739.275
   - MSE = 1,130,745.938
   - RMSE = 1,063.365
   - R^2 = 0.590

- The Final Model Chosen was the Tuned Random Forest Regressor Model with the n_estimators tuned to 200.

- For the testing set on the model, 59.0% of the variance in y was explained by x.

- The Mean Absolute Error was off by about 739.275.

 - The Mean Squared Error was 1,130,745.938 .

-  The Root Mean Squared Error had a calculation of 1,063.365.
   My model’s RMSE of 1,063.365 provides a reasonable estimate of the sales prediction errors.
   On average, the model’s predictions are off from the actual sales by approximately 1,063 units.
   This metric is expressed in the same units as the target which is Outlet-Sales, thus easier for us and our stakeholders 
    to understand as well as apply the perfomamnce assement of the model.

 ## Final Recommendations
 -  Fat Content in items:
    - Consider  stocking more items with low levels of fat since customers have a higher preference for them which in turn 
       maximizes sales.
    - Educate consumers through highlighting the benefits of low fat without compromising on quality.

-  Product Assortment Optimization:
   - Analyze which product types contribute the most to sales.
   - Focus on promoting or stocking these high-impact products.

