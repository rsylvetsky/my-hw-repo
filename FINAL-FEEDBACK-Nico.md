### ***Final Project Feedback***

***Nico Van de Bovenkamp***

***

***Modeling***  
Nice use of the pipelines! You can always use the Sklearn classes if you are in sklearn, but the logic applies in any language: build a set of transformations and pipe them together!

When you are taking the classes, you would want to put `len(set(y_train2))` so you get the number of classes, not the length of the dataframe.

I also think that your models could have benefitted from a good bit more cleaning. It looks like a lot of the negative words your models picked up on look either misspelled or changed words from some of your cleaning steps/stemming. In particular when you notice that you have the name of the class in the text!

***Evaluation metrics***  
When you are working through these models, it's good to diagnose what is going on them. This can be done by using various classification model evaluation metrics/techniques. For one, try out a few metrics (auc, precision, recall, etc.). You can then take a look at your confusion matrix to see what is being misclassified, and how. Then you can take a look at those samples. Spending time with those outputs/models will help you understand both your models AND what's going on in your underlying data. With all of that, try out some plots! Plotting things out will help you pick up on things much fast than just staring at some numbers!

***Features***  
Feature extraction is key in machine learning. As I said, models are important, but good data is much, much more important. With that said, you should try experimenting with extracting different feature sets. In this case, you could experiment with different uses of your TfIdf and CV. In particular, you should play with your n_grams (this will help add some context into your model) and add the removal of stop_words for sure! Stop words, like "the" and "and" and "as" will just add complexity to your model with zero-to-no value. You should also play with the min document frequency parameter for sure! Also, you should certainly strip all integers (digits) from your text. They won't add much value, as your models indicate, but they do add complexity and reduce the impact of the features that do matter.

On a final note, as we discussed, definitely look into word embeddings! Training your own embeddings is hard, but if you have enough data and you clean it well enough, you could make some awesome tweet embeddings that pick up dramatically more non-linearities in the data and make much more complex features.

***Where to go from here***  
Now that you have made it through the course, I am sure you feel like you learned a lot, but have even more to learn. It's almost a bit overwhelming. As I said at the beginning of this course, the part-time course serves as a great base line for you to really start doing the work on your own, or out in the world. Now, what you do next is totally up to you, and totally dependent on where you want to take your skills given this experience. Maybe you want to practice coding and python for automating tasks or working with data. Maybe you want to just learn a bit more so that you have a better understanding of what the analysts, data scientists, and engineers do at work. But if you want to keep learning in this domain, then here are a few of my recommendations:  

* **Practice your programming and software development skills.**  One of the most important things to do as a baseline is just to get better at coding. Find a good book or series of online courses on python, whether it's for data science or just python in general, and dig in. From there, it's all about practice! Knowing some object-oriented programming, networking, working in a cloud environment, potentially some other languages/frameworks like tensorflow, pytorch, and scala, ssh, and other things will get you up to speed in this space.

* **Revisit the basics of statistics, machine learning, and deep learning.** Now that you have gone through all of these different models and approaches at a high level, you should spend some time going back to the basics. You should be able to answer questions like:   
    - what is a loss function?
    - what is supervised vs. unsupervised learning?
    - should you use a more "statistically oriented" model or machine learning model?
    - what are optimization techniques and how are they used?
    - what is the structure of this model?
    - what are common approaches for this problem?
    - what are common sampling techniques?
    - what is cross-validation?  

    Take a look at blogs like **KDNuggets** and various online Data Science community groups to find out what types of questions you should be able to answer!

* **Practice and read all the time!** Nothing beats experience, and there are tons of ways to get it. Go on kaggle and spend some time trying things out on datasets. Find a project at work, or with friends/a group, to work on. Surround yourself with people that are experienced (at work, I am around tons of people that are truly talented, and I learn tons from it!).

**I hope you enjoyed the course! If you have ever have any questions, don't hesitate to reach out via email (nico.vdb@nyu.edu or njvandebovenkamp@gmail.com)**  

**Best,  
Nico**
