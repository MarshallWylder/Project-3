# Patient Survival model

![istockphoto-1194838627-170667a](https://github.com/MarshallWylder/Project-3/blob/main/images/istockphoto-1194838627-170667a.jpeg)

**Author**: Marshall Wylder

## Overview
    
I am analyzing data in order to predict patient survival. I created several tree based models picked the one with the best f1 results that also wasn't overfit. Not being overfit is very important to the business problem because the predictions will be used for actions in life and death scenarios.

## Buiness Problem

I was hired to show a proof of concept for the implementation of modeling patient survival in order to better predict outcomes so treatments and resources can be used to optimize patient survival.

## Data Understanding

I used patient survival data from 2021 from [kaggle](https://www.kaggle.com/datasets/mitishaagarwal/patient). The data used for this modeling include Simple metrics such as height, weight, and age. I also included APACHE III codes (Acute Physiological And Chronic Health Evaluations), which are sub-diagnosis codes which best describe the reason for the ICU admission as well as physiological variables like body temperature, min and max heart rate, min and max respiratory rates, as well as a few others. APACHE IV death probabilities, which is a  prediction of in ICU mortality for the patient which utilizes the APACHE III score and other covariates, including diagnosis were included to as additional death probablilities as features to build off prior informmation. 

## Modeling and Results

My baseline model was dummmy classifier which had a accuracy of .91 but an fi score of zero.   
![Dummy Model](https://github.com/MarshallWylder/Project-3/blob/main/images/Dummy%20model.png)

After several overfitted models my final model is an Extra Tree Classifier with parameters tuned to be more robust against unseen data.
![Final Model](https://github.com/MarshallWylder/Project-3/blob/main/images/Final%20model.png)

The f1 score of this fiinal model is at .50 with the f1 score of the test data was at .46. Althoughthe model is a little overfit I feel confident the model should reproduce consistent predictions with unseen data.

## Next Steps

If the use of predictive model as a tool to help doctors improve patient outcomes interests the hospital, I would recommend hiring a data scientist to maintain and improve these models and deploy system integrations so models can be updated daily with new data to improve accuracy.


```
 ├── data
 ├── images
 ├── Notebook.ipynb
 ├── gitignore
 ├── Survival.pdf
 └── README.md
```
