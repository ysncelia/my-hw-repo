### ***Project 4 Feedback***

***Nico Van de Bovenkamp***

***

**Overall**  
You nailed this assignment! This is exactly the type of thing we would like to see in a final presentation notebook. You walked through the key layout of the problem, your data, your analysis, results, several different classification models, and future things to explore. Awesome!

One quick suggestion might be to present some issues that you ran into when working on this problem (why is this problem... a problem?!). Another recommendation is for a few more plots that are associated with your model.

***Train/Test Split***  
We don't perform this task in the homework (something that I definitely disagree with), but always remember the basics of model validation -- train-test-split! Recall that you always want to prove that your model will generalize well. The standard method for doing so is splitting your data into train set and test set, then performing some cross-validations on the train set. This way, you will be able to justifiably show that the model you have created is, in fact, the best model that you could make. You are dramatically less likely to over-fit to your training data.

***Hyper-parameter tuning***  
It's a bit surprising to me that your model accuracy wouldn't lift from ~69% and the base logistic regression. Though it is possible that these tree based ensemblers will not perform well due to small sample size, it seems slightly unlikely that they would have the same, relatively low, accuracy. Try playing with the default hyper-parameters. I didn't see what yours were, but you should play with the learning rate, max_depth, and the min_sample_leaf for starters. Those ensemblers can be very sensitive to changes here, and given the low sample size AND low rank (small feature set) of this data, the defaults may be improper.
