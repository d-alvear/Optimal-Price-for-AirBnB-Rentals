# Optimal Price for an AirBnB Rental
## Introduction
AirBnB is a marketplace for short term rentals that allows users to list part or all of a living space for others to rent. Users can rent everything from a room in an apartment to your entire house on AirBnB.

## Problem Definition
One challenge that hosts looking to rent their living space face is determining the optimal nightly rent price. In many areas, renters are presented with a good selection of listings and can filter on criteria like price, number of bedrooms, room type and more. Since AirBnB is a marketplace, the amount a host can charge on a nightly basis is closely linked to the dynamics of the marketplace. 

In this project I will be taking on the role of a host wanting to rent my living space. As a host, if I try to charge above market price for my living space, then renters will select more affordable alternatives which are similar to mine. If I set my nightly rent price too low, I could miss out on potential revenue.

One strategy I could use is to:

* find a few listings that are similar to mine (k=5),
* average the listed price for the ones most similar to mine,
* set my listing price to this calculated average price.

In this project I will use data on local listings to predict the optimal price to set for a rental. I will use the K-Nearest Neighbors algorithm to solve this problem.

## Modeling

When fitting the KNN model on the `accomodates` and `bathrooms` features, I got an RMSE of $214. This was a large error so I decided to use more features in the model. Including `bedrooms` and `number_of_reviews` as model features, then retraining the KNN model, decreased the RMSE to $207. I then trained a model using the rest of the features to see if this would improve the performance even more. The KNN model trained with all features increased the error to $213.
