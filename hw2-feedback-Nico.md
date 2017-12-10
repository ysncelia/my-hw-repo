### ***Project 2 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:** Awesome job on this homework! You did a great job at outlining tour analysis, using python to break down your dataset, and even tried your own model out! Keep this up! I made some notes below on some of the concepts you should make note of regarding modeling. We will cover this more in subsequent classes, so it will become much more clear. Also, as you mentioned, keep on trying to take full advantage of Python! Try writing out your own functions to perform tasks as we do in class! For example, we had that `.get_model_metrics()` method so we could input a model and data, and then we get metrics, parameters, and a nice graph all in one go!


**Some Notes**

* Nice call out with the Variation Inflation Factor! This is a handy test, and statsmodels actually has an implementation that you can use. Check out this [walkthrough here](https://etav.github.io/python/vif_factor_python.html).
* We haven't covered the specifics quite yet, but we won't be using a linear _regression_ model in this example. We will be using a linear model, but it will be a logistic regression, which is a classification technique. Remember that a regression model _usually_ refers to a model that is learning a continuous variable (income, temperature, whatever!) whereas a classification model refers to predicting classes, like our admission (yes or no!). But good work on trying your hand at the OLS!!
* Also, typically in a classification problem, as explained above, you wouldn't use an evaluation metric like R^2 as that is mostly used for regression tasks. We will cover this later in class, but maybe you would use something like accuracy, f1 score, precison, recall, and some other metrics!  

**Something to think about**

***Imports***  
So I know you mentioned that you were confused about import statements in Python. Let's walk through the imports in the starter-code so that you know what is in each one:

```python
#imports
from __future__ import division
# __future__ is a class that is built from the base of python. All python   
# code has this, but you import division from the python main library so that
# you have it for later use. It is similar to doing an import String!
import pandas as pd
# This is the main library that we use for our data manipulation
import numpy as np
# This is a great library for Numeric python. It is used for scientific
# computation. Look to this for arrays random variables, array operations,
# and math functions!
import matplotlib.pyplot as plt
# Our main plotting library!
import statsmodels.api as sm
# This is the library that is used for statistics in python.
# You can use this for logistic regression, OLS, and other statistical
# models like we did in class with OLS!
import pylab as pl
# This is kind of a weird library for a combination of plotting and sci-py!
# It's not essential.
%matplotlib inline
# This line is used as an expression in Jupyter Notebooks so that you can
# see plots output in the cells of your notebook.
```

Dropping missing values can be necessary at times. In cases where you you have a lot of missing values, you might have to just drop those rows *or* ignore that feature all together (forget that column, we can't use it). However, as we proceed, you will find that data is gold to these algorithms. Very often, the more data you have, the more information you are giving to your model so it can generalize even better. To ensure we retain as much data as we can, a common practice is to fill missing values with the mean or median or mode so that you can keep those instances, without disturbing your distribution too much. Check out these guides:
https://machinelearningmastery.com/handle-missing-data-python/
https://chrisalbon.com/python/pandas_missing_data.html
