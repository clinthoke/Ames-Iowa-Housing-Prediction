# Predicting Housing Prices in Ames, Iowa

#### Executive Summary

In this project, I explored data on housing prices on properties sold in Ames.  The data set takes Home prices and related housing data from 2006 to 2010, and I used it to build a model for predicting individual housing prices. I used EDA, feature engineering and linear regression to build my model.

---

#### Problem Statement

As the Iowa Association of REALTORS® (IAR), our mission statement is to: "To be Iowa’s trusted voice for real estate, and empower members and associations to achieve excellence."  We are hoping to introduce a new feature, called 'Priced Right', on our website to support our realtors. 'Priced Right' will predict the selling price of a house that our agent is putting on the market. 'Priced Right' will allow our agents to pick a sell price at the height of its selling range, or know where to price a home for a quick sell. Our agents need every advantage to compete with our big competitors like Re/Max, Keller Williams and Century 21. We hope that developing this tool gives our relators the best information possible. This presentation will cover our initial findings based on past data and plans for the project going forward if 'Priced Right" is approved to move forward.

All of my external research and resources came from this website:  https://www.iowarealtors.com/about-us

---

#### Data Import and Cleaning

The data that was provided was housing data for individual houses sold from 2006 to 2010.  This data was sectioned into a training set and testing set.  There was information provided on 2051 houses sold with 79(81 Columns) features for each sale.
https://www.kaggle.com/c/dsir-420-project-2-regression-challenge/data

For this project, we are preparing submissions to Kaggle to score the competition

Data cleaning was performed in the accompanying python notebook. The training and testing were both cleaned uniformly.

---

#### Data Exploration and Analysis

I calculated statistical information about each category and rand distributions on important categories. Data trends were investigated and various features were added and taken away based on the RMSE of the SalesPrice.

---

#### Data Visualization

I created a Heat Map, histograms, bar plots, and scatter plots and visualize determine correlations in the data.

This one column correlation heatmap shows the top correlated features when compared to SalesPrice.  These were the main features I concentrated on in modeling my data.




![Correlation for SalesPrice](https://i.imgur.com/pz5xWv0.png)


---

#### Data Dictionary

Sample Data Dictioary

|Feature|Type|Description|
|---|---|---|
|SalesPrice|int|The selling price of the home.| 
|Total SF|int|Combination of the Total Bsmt SF,1st FlrSF, and the 2nd Flr SF|
|TotRms AbvGrd|int|Total rooms above grade (does not include bathrooms)|
|Overall Qual|int|Rates the overall material and fini|
|Garage Area|int|Size of garage in square feet|
|Year Built|int|Original construction dateRemodel date (same as construction date if no remodeling or additions)|
|Mas Vnr Area|int|Masonry veneer area in square feet|
|Neighborhood_Blmngtn|Boolian|Physical locations within Ames city limits|
|Year Built_log|int|The log of the Year Built Column|



---

### Takeaways


My models used linear regression to chose the features that most affect sales price.  The Total SF, Overall, Gr Liv Area, Garage Area, and Year Built are the features that had the most effect on the model. I added in features and took others out to refine the model to improve the RMSE.


---

### Next Steps




Updated data is the first issue that needs to be addressed.  The most recent data we have is from 2010 and our future models need to be based un updated info. Neighborhoods change over time as houses get older and new neighborhoods are built.  Inflation will have also increased house prices since 2010 and that needs to be accounted for.  Also, factors that people look for in houses change over time. Changes in these factors will influence the model and will need to be accounted for. I hope to import new features like school rankings, location of the laundry room and HOA association and fees from MLS to aid in the model.

Also, this model is a bacsic linear regression model that was just a base to start the project.  More models like LASSO, Ridge, XGBoost or Neural Networks will be used to refine the project.