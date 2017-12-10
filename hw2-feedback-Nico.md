### ***Project 2 Feedback***

***Nico Van de Bovenkamp***

***

**Overall:** Great job on this homework! You are clearly quite comfortable with most of these concepts, and you are playing with different methods to hack away at data. Keep this up and explore different ways to use all of Python to write more efficient code and process data. Maybe play with writing your own functions to perform tasks! Also, let me know if you have any questions on modeling, as this is the next **big** section in our journey!


**Some Notes**

* I find this a really weird subtle point, but skew is actually in the direction of the long tail, thus the skew in those features is actually to the left. Weird, I would also think sometimes that the skew would be in the direction of the bulk of a distribution, but it's more of a statement of outliers.
* *Q.10:* You could definitely use the central limit theorem, yes! But, for modeling purposes, you could also do some kind of transform on the data like we did in class. I think you wrote this before we did the examples in class, but recall the transforms that we did in class with log. You could do any kind of transform though!
* Regarding co-linearity, there really ins't any hard-set rule... In general though, something like `r>0.5` would indicate some level of co-linearity. Most often, you will make note of this then continue in your analysis. As we had done in class, you will find that adding or dropping certain features will result in different levels of significance for predicting an outcome. So, if you notice that GRE is insignificant, but GPA is significant, then maybe GRE is in fact highly correlated with GPA and it wouldn't help you. In this case, correlation is low, so you will have some information encoded in GPA that you wouldn't in GPA.
* Regarding your analysis plan, you should probably include what models/modeling techniques you think you would use. Considering we haven't gotten into it yet, this is more than okay to not include yet. However, typically when you write out your analysis plan, you include data cleaning, data manipulation, some analysis, and then modeling techniques to find, in this case, the relationship between Admission and Prestige!
* Regarding that `for` loop at the end, this should work, but the issue isn't in the loop, it's in data types... This is an insight into data types into python, but: type `None` is a Python data type that is different from type 'NaN' which is a `np.nan`. This means that `np.nan != None`. The values that are missing in pandas dataframes there are `np.nan`. If you replace `None` with `np.nan`, this should work! Also, note that you shouldn't write explicit for loops for these operations. These will be fairly slow. What you could do is use an [`.apply()` method](https://chrisalbon.com/python/pandas_apply_operations_to_dataframes.html). These work much faster because they perform array operations and work more directly in numpy, not Python.

**Something to think about**  
Dropping missing values can be necessary at times. In cases where you you have a lot of missing values, you might have to just drop those rows *or* ignore that feature all together (forget that column, we can't use it). However, as we proceed, you will find that data is gold to these algorithms. Very often, the more data you have, the more information you are giving to your model so it can generalize even better. To ensure we retain as much data as we can, a common practice is to fill missing values with the mean or median or mode so that you can keep those instances, without disturbing your distribution too much. Check out these guides:
https://machinelearningmastery.com/handle-missing-data-python/
https://chrisalbon.com/python/pandas_missing_data.html
