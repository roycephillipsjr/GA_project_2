# Ames Housing Project

## Problem Statement
Using data Ames Housing dataset from Kaggle. The goal is to create the best model to predict the price of a home in Ames Iowa.
Trying to find the best features that will increase the value of a home.

## Executive Summary
Looking through this notebook you can see all the information you need to find on how I came to my conclusion. The data is taken from a Kaggle competition. The dataset is the Ames Housing data which has home features and the price it sold for from 2006-2010. 
Below you can see all the resources and the work that was done on the data. It includes:
1. A folder of code with 3 jupyter notebooks
2. The data sources including the original source and my clean data.
3. Articles referenced for the powerpoint presentation
4. A data dictionary
5. The procedure and methodology
6. The conclusion

## Contents:
### Folders
- [Code] 
--- [EDA and Cleaning] (01_EDA_and_Cleaning)
--- [Plotting and Graphs] (02_Plotting_and_Graphs)
--- [Modeling] (03_Modeling)
- [Project 2 Ames PPT](#Project_2_Ames_Housing.pptx)

## Data sources:
- [Clean Ames Housing Data](../datasets/clean_ames_housing_data.csv)
- [Submissions](../datasets/submission.csv)
- [Test Data](../datasets/test.csv)
- [Training Data](../datasets/train.csv)
- [Sample Submision Regression](../datasets/sample_sub_reg.csv)

## Articles referenced

- [What is EIFS - Synthetic Stucco?] (https://www.thebalancesmb.com/eifs-synthetic-stucco-1797883)
- [Synthetic versus Traditional Stucco Siding](https://www.homeadvisor.com/r/synthetic-versus-traditional-stucco-siding/)
- [Average Weather in Ames](https://weatherspark.com/y/10339/Average-Weather-in-Ames-Iowa-United-States-Year-Round)


Feature|    Type|    Dataset|Description|
-------|--------|-----------|-----------|
**Id**|integer|Ames Housing|Observation number|
**PID**|integer|Ames Housing|Parcel identification number - can be used with city web site for parcel review.|
**MS Zoning**|object|Ames Housing|Identifies the general zoning classification of the sale.
**Lot Frontage**|float|Ames Housing|Linear feet of street connected to property|
**Lot Area**|integer|Ames Housing|Lot size in square feet|
**Street**|object|Ames Housing|Type of road access to property|
**Lot Shape**|object|Ames Housing|General shape of property|
**Land Contour**|object|Ames Housing|Flatness of the property|
**Utilities**|object|Ames Housing|Type of utilities available|
**Lot Config**|object|Ames Housing|Lot configuration|
**Land Slope**|object|Ames Housing|Slope of property|
**Neighborhood**|object|Ames Housing|Physical locations within Ames city limits|
**Condition 1**|object|Ames Housing|Proximity to various conditions|
**Condition 2**|object|Ames Housing|Proximity to various conditions (if more than one is present)|
**Bldg Type**|object|Ames Housing|Type of dwelling|
**House Style**|object|Ames Housing|Style of dwelling|
**Overall Qual**|integer|Ames Housing|Rates the overall material and finish of the house|
**Overall Cond**|integer|Ames Housing|Rates the overall condition of the house|
**Year Built**|integer|Ames Housing|Original construction date|
**Year Remod/Add**|integer|Ames Housing|Remodel date (same as construction date if no remodeling or additions)
**Roof Style**|object|Ames Housing|Type of roof|
**Roof Matl**|object|Ames Housing|Roof material|
**Exterior 1**|object|Ames Housing|Exterior covering on house|
**Exterior 2**|object|Ames Housing|Exterior covering on house (if more than one material)|
**Mas Vnr Type**|object|Ames Housing|Masonry veneer type|
**Mas Vnr Area**|float|Ames Housing|Masonry veneer area in square feet|
**Exter Qual**|integer|Ames Housing|Evaluates the quality of the material on the exterior 
**Exter Cond**|integer|Ames Housing|Evaluates the present condition of the material on the exterior|
**Foundation**|object|Ames Housing|Type of foundation|
**Bsmt Qual**|integer|Ames Housing|Evaluates the height of the basement|
**Bsmt Cond**|integer|Ames Housing|Evaluates the general condition of the basement|
**Bsmt Exposure**|integer|Ames Housing|Refers to walkout or garden level walls|
**BsmtFin Type 1**|integer|Ames Housing|Rating of basement finished area|
**BsmtFin SF 1**|integer|Ames Housing|Type 1 finished square feet|
**BsmtFinType 2**|integer|Ames Housing|Rating of basement finished area (if multiple types)|
**BsmtFin SF 2**|float|Ames Housing|Type 2 finished square feet|
**Bsmt Unf SF**|float|Ames Housing|Unfinished square feet of basement area|
**Total Bsmt SF**|float|Ames Housing|Total square feet of basement area|
**Heating**|object|Ames Housing|Type of heating|
**HeatingQC**|integer|Ames Housing|Heating quality and condition|
**Central Air**|integer|Ames Housing|Central air conditioning|
**Electrical**|object|Ames Housing|Electrical system|
**1st Flr SF**|integer|Ames Housing|First Floor square feet|
**2nd Flr SF**|integer|Ames Housing|Second floor square feet|
**Low Qual Fin SF**|integer|Ames Housing|Low quality finished square feet (all floors)|
**Gr Liv Area**|integer|Ames Housing|Above grade (ground) living area square feet|
**Bsmt Full Bath**|float|Ames Housing|Basement full bathrooms|
**Bsmt Half Bath**|float|Ames Housing|Basement half bathrooms|
**Full Bath**|integer|Ames Housing|Full bathrooms above grade|
**Half Bath**|integer|Ames Housing|Half baths above grade|
**Bedroom AbvGr**|integer|Ames Housing|Bedrooms above grade (does NOT include basement bedrooms)|
**Kitchen**|integer|Ames Housing|Kitchens above grade|
**KitchenQual**|integer|Ames Housing|Kitchen quality|
**TotRmsAbvGrd**|integer|Ames Housing|Total rooms above grade (does not include bathrooms)|
**Functional**|object|Ames Housing|Home functionality|
**Fireplaces**|integer|Ames Housing|Number of fireplaces|
**FireplaceQu**|integer|Ames Housing|Fireplace quality|
**Garage Type**|object|Ames Housing|Garage location|
**Garage Yr Blt**|integer|Ames Housing|Year garage was built|
**Garage Finish**|integer|Ames Housing|Interior finish of the garage|
**Garage Cars**|float|Ames Housing|Size of garage in car capacity|
**Garage Area**|float|Ames Housing|Size of garage in square feet|
**Garage Qual**|float|Ames Housing|Garage quality|
**Garage Cond**|integer|Ames Housing|Garage condition|
**Paved Drive**|object|Ames Housing|Paved driveway|
**Wood Deck SF**|integer|Ames Housing|Wood deck area in square feet|
**Open Porch SF**|integer|Ames Housing|Open porch area in square feet|
**Enclosed Porch**|integer|Ames Housing|Enclosed porch area in square feet|
**3-Ssn Porch**|integer|Ames Housing|Three season porch area in square feet|
**Screen Porch**|integer|Ames Housing|Screen porch area in square feet|
**Pool Area**|integer|Ames Housing|Pool area in square feet||
**Fence**|integer|Ames Housing|Fence quality|
**Mo Sold**|integer|Ames Housing|Month Sold (MM)|
**Yr Sold**|integer|Ames Housing|Year Sold (YYYY)|
**Sale Type**|object|Ames Housing|Type of sale|
**SalePrice**|interger|Ames Housing|Sale price $$|

## Procedure/Methodology
The biggest hurdle for the project was learning to deal with such a large dataset. At least this was the largest I have dealt with so far. There were originally 80 columns all with unique features. 
The first thing that I had to do was to load in the data and do a quick glace at what how the data was structured. The thing that was immediately noticable was how many missing values there were. 
I then started cleaning the data as best as I could breaking it down into small sizeable chunks. The first thing I noticed was a correlation between missing values in the garage column, but also have no square footage. Since the values were missing for example in garage type, but a 0 given in the square footage I infered that there was no garage. So all the garage variables that had no values I imputed zeros into them. 
I continued imputing values into other columns like all the basement varities.
As I was slowly cleaning the data I would periodically put the completed values into a heatmap to see how those variables would affect the price of a home. I was slowly trying to think of things I could put into my model. I would also make a couple of scatter plots to see if I could feature engineer some new values to see how it affected the data.
After completely cleaning all the data I went full steam ahead on plotting all the data on as many different graphs and scatterplots as I could to see if I noticed any strong trends.
Once I saw many strong trends I started creating my models and slowly iterated them the get better and better. After all the work the best I got was an 89% on the test data.

# Conclusion/Recommendations
In conclusion, even though this data was very large and had many variables that could affect the cost of the home. It really came down to a handful that really did drastically affect the cost of a home.
The greatest factors were the overall quality, the total sqaure footage of the home, exterior quality, and the neighborhood the house was in. 
Things that people can do to increase the value of a home is fully furnishing the basement, which includes a full bath, making sure there is a least 1 fireplace(a max of 2), and having a good size garage.
These are the things that will greatly affect the cost of a home. 