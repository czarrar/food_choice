# Determinants of Food Choice in a Large US sample

## Intro

Food-based tasks are commonly used to study mechanisms of eating disorders. To better understand the determinants of food choice, we studied how a wide range of individuals characterize foods and make food-based decisions. These data can be useful in a wide array of contexts including public health decisions on obesity and/or improved marketing to match foods based on consumer preferences.

## Methods

In this large, online study of the general population (N = 1,075, 50% female), participants were shown images of food (45 per participant, 138 total). Each food was rated on 17 different attributes (health, taste, etc). Participants then completed a food choice task. Ratings/choices were done on a continuous slider scale (0-1). There was no time limit on a response.

<p align="center">
  <img src="https://github.com/czarrar/food_choice/blob/master/images/methods.png" width="800" >
</p>

## Sample

* There was an equal number of male and female participants.
* Majority had a college degree and were employed.
* Median income was $50-70,000
* BMI ranged from 17.7-80.8 kg/m2 and age ranged from 18-75 years.

The plots from the demographic data can be found in `10_demographics.html`.

## Food Ratings

Ratings for each individual food item were averaged across subjects. Pairs of group-average ratings were correlated.

<p align="center">
  <img src="https://github.com/czarrar/food_choice/blob/master/images/food_rating_correlations" width="800" >
</p>

Positive values are shown in red and negative values are shown in blue. Higher values are shown as larger and darker circles.

A factor analysis identified 3 components among the ratings: sensory experience (taste, texture, etc), nutritional content (health, vitamins, etc), and unami flavor (savoriness,  protein, etc). Number of factors were determined by the CNG index.

<p align="center">
  <img src="https://github.com/czarrar/food_choice/blob/master/images/food_rating_factors" width="700" >
</p>


## Food Choice

> Used a mixed-effects linear regression in R. Model included taste, health, protein ratings and interaction of each rating with BMI, gender, and age.

Using each factor score to predict choice, we found that foods rated as tasty (p < 0.001) and protein-rich/not-sugary (p < 0.05) were more likely to be chosen while health-related ratings did not influence choices (p = 0.83).

<p align="center">
  <img src="https://github.com/czarrar/food_choice/blob/main/30_food_choice_files/figure-html/unnamed-chunk-7-1.png" width="300" >
  <img src="https://github.com/czarrar/food_choice/blob/main/30_food_choice_files/figure-html/unnamed-chunk-7-2.png" width="300" >
  <img src="https://github.com/czarrar/food_choice/blob/main/30_food_choice_files/figure-html/unnamed-chunk-7-3.png" width="300" >
</p>

Foods rated as healthy were less likely to be chosen by men (p < 0.01) and individuals with higher BMI (p < 0.05). In contrast, foods rated as healthy were more likely to be chosen by older adults (p < 0.001) and such healthy foods were more likely to be rated as tasty by older adults (p < 0.05). See the `30_food_choice.*` file.

## Conclusions

This study characterizes attributes and decision making across food images representative of a normal diet, in a large group of individuals, providing broader context to food choices in healthy and unhealthy eating.
