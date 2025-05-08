# The Elo System: The Best K For You

If you are working on a project where you would like to compare performance - be that of teams, players, or products - this repository contains the code for the Elo method. Elo was originally built for chess but can work with anything that you can assign a ‘win’, ‘loss’, or ‘tie’ between two objects. This repository contains Jupyter notebooks for a base Elo system, where you’ll find the standard K value is 32. This is a default value, but may not be the best for your dataset. The other two Jupyter notebooks serve to find that best K value for your dataset. The two do a similar job but with a slightly different goal. OptimizeK_FullTraining is a more general approach to finding your best K.

Those Reasons may include:

If you want to create a system that is biased by more recent games, increase K.

If you want if you want a system that feels the impact of order less,  lower $K$. 

If you expect future games to be more random, perhaps due to injuries, lower $K$. This change can be done in the short-term or long-term.

If you expect a shorter season, due to a lockout, increase K from what you'd typically see.


## Elo
This notebook contains the code for running an elo system. The K value will default to 32, but you are encouraged to use the other two codes to find the best K for your dataset. You can also make additional, manuel fine-tuning to your K value.

## OptimizeK_FullTraining

This notebook will take in your dataset, and it will find the K value that leads to the final elo ratings that best fit the data. This also runs the Elo system at that K value.

Compared to OptimizeK_OnTheGo, this notebook is a more standard approach to optimizing K. It takes in all the training information, then produces the best end Elo ratings based on that.


## OptimizeK_OnTheGo
This notebook will take in your dataset, and it will find the K value that leads to the Elo ratings best fitting the data at all points throughout the season. This notebook also runs the Elo system at that K value. This notebook also has the build-in property of choosing how much you want the system to remember. If you only want a certain amount of recent games to be relevant to the ratings, you can optimize K on the go for that amount of games to get that property.

Compared to OptimizeK_FullTraining, this method for optimizing K will value its accuracy at all points in the season, so it produces the K that is the most accurate to the outcome of every game at the time of the game.
