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
| wine_quality.ipynb        | Main file containing the cleaning, creation of the different models, and visuals. |
| wine.csv      | Original csv file with information about wines |
| Visuals           | Directory containing images             |

# Project evolution
![](Visuals/All_evolution.png)

## v0 (Baseline)
* No manipulation of data
* Separation of 'bad'(quality < 6) and 'good' (quality >= 6) wines
* Great unbalance of bad (2384) and good (4113) wines
* Overfitting

|    | Loss      | Accuracy | Val Loss | Val Accuracy | Test Accuracy |
| -- | --------- | ------   | -------- | ------------ | ------------- |
| v0 | .56       | .69      | .55      | .70          | .71           |

![](Visuals/0_Accuracy_Loss.png)
![](Visuals/0_Confusion_Matrix.png)

## v3 (Final)
* Separation of 'bad'(quality < 7) and 'good' (quality >= 7) wines
* Great balance of bad (5108) and good (5220) wines

|    | Loss      | Accuracy | Val Loss | Val Accuracy | Test Accuracy |
| -- | --------- | ------   | -------- | ------------ | ------------- |
| v0 | .56       | .69      | .55      | .70          | .71           |

![](Visuals/3_Accuracy_Loss.png)
![](Visuals/3_Confusion_Matrix.png)

# Timeline
07/09/2021 - 09/09/2021