# Deep learning - Wine Quality challenge
![](Visuals/wine_banner.jpeg)
# Mission
Create an AI model to predict the quality of a wine. By using an AI model, we would reduce the risk of bias, usually associated with wine tasting.

# Goal
* Use a deep learning library
* Prepare a data set for a machine learning model
* Put together a simple neural network
* Tune parameters of a neural network

# Installation
### Python version
* Python 3.9

### Packages used
* pandas
* matplotlib
* seaborn
* sklearn
* tensorflow

# Usage
### Main folder
| File           | Description                                                 |
|-------------------|-------------------------------------------------------------|
| wine_quality.ipynb        | Main file containing the creation of the different models, and visuals. |
| wine.csv      | Original csv file with information about wines |
| Visuals           | Directory containing images             |

# Project
## Project evolution
![](Visuals/All_evolution.png)

## Intro
* All models are Sequentials and used Dense layers
* Always Relu as activation function, except the output layer with Sigmoid

## v0 (Baseline)
* No manipulation of data
* Separation of 'bad'(quality < 6) and 'good' (quality >= 6) wines
* Great unbalance of bad (2384) and good (4113) wines
* 2 hidden layers (20, 10)
* Epoch = 30

|    | Loss      | Accuracy | Val Loss | Val Accuracy | Test Accuracy |
| -- | --------- | ------   | -------- | ------------ | ------------- |
| v0 | .56       | .69      | .55      | .70          | .71           |

![](Visuals/0_Accuracy_Loss.png)
![](Visuals/0_Confusion_Matrix.png)

## v3 (Final)
* Separation of 'bad'(quality < 7) and 'good' (quality >= 7) wines. Better predictions!
* Great balance of bad (5108) and good (5220) wines (upsampling)
* After trials and errors, here are the best parameters found (for accuracy)
* 4 hidden layers (30, 30, 20, 10)
* Epochs = 300
* Early stopping used to prevent overfitting

|    | Loss      | Accuracy | Val Loss | Val Accuracy | Test Accuracy |
| -- | --------- | ------   | -------- | ------------ | ------------- |
| v3 | .35       | .83      | .48      | .77          | .78           |

![](Visuals/3_Accuracy_Loss.png)
![](Visuals/3_Confusion_Matrix.png)

# Remarks
* Lower results when normalising the data, so kept the data as it is
* Tried feature engineering by adding the type of wine (red or white) and creating a sulfate ratio, but it didn't improve the model
* More layers, more neurons, more epochs did improve the model's accuracy, but overfitting did happen sometimes. Had to look at both the accuracy and loss metrics, as well as the confusion matrix to get a good overview.
* Random Forest model has very high accuracy (0.96) on this dataset
* KNN also has high accuracy (0.94)

# Timeline
07/09/2021 - 09/09/2021