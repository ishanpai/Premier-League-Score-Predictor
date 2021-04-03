# Premier-League-Score-Predictor

Overview
This data science project aims to predict the outcome of premier league matches for gameweek 30 by giving teams an attack rating (based on goals scored and xG) and a defense rating (based on goals conceded and xG against). The rating also takes into account form, giving more recent matches more importance than matches well in the past. We start with a very simple model and build up towards more detailed models that would better capture the parameters that would affect the score of a football match.

This model is still just a preliminary idea and a lot of the hyper-parameters should be trained such as how fast the weights decay, the thresholds for predicting wins, draws, and losses. Many more factors should also be taken into consideration such as past results from the same fixture, player injuries, etc. This has the potential of being further expanded upon to get a nice classification model that would predict every match as a home win, draw or away win.

Final Model
We find the probability of a home win, a draw, and an away win so that we can compare with betting websites. We then look at these as theoretical values and would bet accordingly. For example, if the probability implied by the betting odds are much lower than that given with the model, we would want to be on that result. We also find probabilities for the total number of goals in a match, and the win margin.

We see that we have many hyperparamters here that should be tuned: correlation (between home and away goals), xG_importance (amount of weight we give to xG), com (decay of weights). We would ideally perform a grid search to optimize over these parameters but I don't currently have a nice framework to quantify the performance of the model.
