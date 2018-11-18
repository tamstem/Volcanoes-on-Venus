# Volcanoes-on-Venus

ML code to detect volcanoes on Venus

Dataset: https://www.kaggle.com/fmena14/volcanoesvenus

Input data are 110x110 images (one row with 12100 columns) which contain none, one or more volcanoes. 

Targets are:
-Volcano?: are there volcanoes on the image (1 or 0)
-Type: 1 = definitely a volcano,2 = probably, 3 = possibly, 4 = only a pit is visible
-Radius: the radius of the volcano in the center of the image
-Number Volcanoes: The number of volcanoes in the image

If  Volcano?=0, Type, Radius and Number Volcanoes have values nan

First we will predict if there is a volcano in the image using CNN and then we will separate Type, Radius and Number Volcanoes for images withVolcano?=1 and predict their values:
 - Type and Number Volcanoes predicted using Logistic regression
 - Radius predicted using GradientBoostingRegressor
