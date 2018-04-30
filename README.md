
#### About the Project
In this project I used R to do Analysis of **Red Wine Data** which contains 1,599 red wines with 11 variables on the chemical properties of the wine. My focus is to see how each chemical component influences the quality of wine (0 'very bad' to 10 'very excellent'). I made a model to predict the quality of Red Wine. This dataset is public available for research. The details are described in [Cortez et al., 2009].

#### Process I have followed for analysis of RedWineQuality

I visualize each variables to see how they are distributed, using  ggplot2, RColorBrewer libraries. Saw relation between quality and other variables because my target variable was quality, and wanted to see how good the other variables are predictor of quality of wine. I did transformation to see if I can increase correlation coefficient between them. I used GGally library to see correlation. Used caret and MASS packages to make data partition for model building. Used stepwise variable selection method to choose best predictor of wine quality. Found some unusual way of rating, which I have explained on the end of this document.


**R Libraries I Used**

- ggplot2
- grid
- gridExtra
- RColorBrewer
- GGally
- caret
- lattice
- MASS

#### Data Set I used

- wineQualityReds.csv


_**The .ipynb file contains all the analysis process and code I used**_


**_What I found from the Analysis of this dataset?_**

 - For the whole data set most of the people gave rating 5 and 6.
 - Nobody gave rating 0, 1, 2, 9, 10. This might be because most of the people randomly choose the rating 5 and 6.
 - And surprisingly no body rated 9 and 10 means the wine quality might not be good in reality.
 - I first thought that acidity has predictive capability.
 - As quality increases with increase value of citric acid and decreases with increased value of volatile acidity.
 - For residual sugar nobody gave rating 3 and 8 for the value greater than 6.8.
 - May be only one people gave rating 4 for residual sugar value greater than 6.8.
 - Most of the rating 5 falls below the alcohol value 11.
 - Most of the rating 7 lies above the alcohol value 11.
 - Rating 4, 6 are randomly distributed.
 - The interesting fact is for the total.sulfur.dioxide value from 99 to 153 people gave rating 5 except of some outliers.
 - People gave high rating for low value of pH.
 - No people rated 8 for having chloride value greater than 0.121.
 - For sulphate value greater than 0.94 people did not give rating 3.
 - May be only one people gave rating 8. Most of the people gave rating 4.
 - Density showed predictor for quality as it has trend. For higher value of density, quality is low and for lower value of density, quality is high.
 - The linear model gave me seven final variables (volatile.acidity, log10(chlorides), free.sulfur.dioxide, total.sulfur.dioxide, pH, log10(sulphates), alcohol) for prediction of quality of wine.
 - But it is not the final conclusion.
 - There might be other variables(which are not present in our data) we need to consider for wine quality prediction.
