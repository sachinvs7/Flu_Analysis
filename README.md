# Vaccine_Analysis
# Predicting Flu and H1N1 Vaccinations


## Machine learning case study that seeks to predict whether an individual is likely to receive an H1N1 and/or flu vaccine based on their behavioral, socioeconomic, and geographical conditions. Implemented as a team towards a term project for the CISC 873 course (Topics in Advanced Data Analytics)@ Queen's University, Winter 2022. Other team members: Katherine Williams, Shreyansh Anand. Grade received: A+ (15/15) 


## Data: 
Fetched from Centre for Disease Control (CDC); https://www.cdc.gov/nchs/nis/data_files_h1n1.htm after investigating multiple sources. 
The data is from the National 2009 H1N1 Flu Survey (NHFS), a large telephonic survey of households with the target demographic being United States residents, living 6 months or up at the time of the interview. It has 171 attributes, which corresponds to all of the asked questions and responses from 70944 individuals. The majority of the data points are binary values, indicating a yes or no answer, but there do exist several questions which require a categorical response or a numerical range as well as attributes appended by the CDC. Focused on two indicators as dependent variables to represent receiving/not receiving the H1N1 and seasonal flu vaccines.

## Few challenges encountered and mitigated:

1. Significant amount of missing values
2. A majority of the individual features were binary which created a very sparse representation. This naturally not only hindered prediction performance but also
increased complexity with memory/time issues, particularly for our imputation efforts that had to be pivoted twice.
3. A large number of the values/responses from this government public survey were encoded across different
data types incorrectly. 
4. Another issue we faced was that the two dependent variables being predicted were very different in terms of class imbalance. The H1N1 class variable is very imbalanced while seasonal flu is not. This was problematic because any class balancing technique(s) to improve the distribution in H1N1 and thereby heighten performance shouldn't compromise the seasonal flu class.

## Techniques explored and applied:

1. Boxplots, Correlation Analysis, Kurtosis, and Skewness of features
2. MICE and K-NN imputations
3. Sampling 
4. PCA
5. Random Forst and Gradient Boosting Tree models. Flu vaccine intent was met with an Accuracy and F1 score of 90%; for the H1N1 vaccine - 91% and 86% respectively 
6. Exploring model feature importance etc. 

## Breakdown of files:
1. A final project report (CISC_451_839_Project_Final_Report.pdf)
2. The main dataset (h1n1_flu_main_dataset.csv)
3. The imputed dataset (imputed_data_h1n1_flu.csv)
4. A main .ipynb notebook that can be loaded into to Google Colab or an environment of choice along with the above 2 .csv files.
5. Another .ipynb notebook that contains the K-NN imputation code that uses the main dataset for imputation (can take time).
