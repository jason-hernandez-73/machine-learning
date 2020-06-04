# machine-learning with Kepler

This uses the Kepler exoplanets dataset from Kaggle. The dataset classifies possible exoplanets as Candidate, False Positive, or CONFIRMED. Which variables are important in making this determination? Can the machine be taught to make these determinations?

Much of the data is valuable to planetary and stellar research, but not directly releveant to whether a given candidate is or is not a planet. The characteristics of the host star, for instance, may help to understand if a given planet might be capable of supporting life, but do not determine whether an orbiting body is a planet.

Model 1 chose only the "false positive flags," that is, chatacteristics that suggest that a given candidate may, in fact, be a binary star. Considering that random guessing among three possibilities should yield, on average, 33.33333% correct guesses, the score of 75% is a nearly 42% improvement. 

Model 2 chose the false positive flags plus most of the features of the candidate, and brought the score up to over 80%. Model 3 tried to fine tune which features were chosen, so as to speed up the model but maintain a high score. The result of 76% was little better than the false positive flags alone.

In choosing which data to use, it helps to know something of the subject. Diameter and temperature are likely to be important in this case: in our solar system, Jupiter, the largest planet, is large enough that it could be a small star if it was hotter, but it is not hot enough. There should be a range of expected sizes and temperatures distinguishing planets from stars.
