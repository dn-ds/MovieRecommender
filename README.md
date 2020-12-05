# MovieRecommender
---

For a quick summary of the project, see these
[slides](slides.pdf).

### What is MovieRecommender?
---

A 
[web app](http://www.movierecommender.net) 
that makes movie recommendations based on ratings supplied by the user.


### How to use MovieRecommender?
---

To receive movie recommendations, rate the given fifteen movies, and click 
'Recommend Movies'. You will be shown fifteen movie recommendations.

<img src='images/landing_page.png' width='100%' height='100%'>


### How does MovieRecommender work?
---

Behind MovieRecommender is a machine learning model trained on the
[MovieLens](http://grouplens.org/datasets/movielens/latest) 
dataset. When you submit your ratings, the information
is preprocessed using 
[jQuery](http://jquery.com)
and 
[PHP](http://www.php.net),
and then passed onto the machine learning model. The model then processes your
data and returns recommendations. The model is deployed on an 
[AWS](http://aws.amazon.com)
(Amazon Web Service) EC2 (Elastic Compute Cloud) t2.micro instance using the 
[Flask](http://palletsprojects.com/p/flask)
framework. 

### How was the machine learning model built, and what is included in this repository?
---

The machine learning model was trained on the
[MovieLens](http://grouplens.org/datasets/movielens/latest) 
dataset, which consists of 27,753,444 movies ratings created by 
283,228 users between January 09, 1995 and September 26, 2018.

The goal of the machine learning model is to make movie recommendations
based on ratings supplied by a user. 

Our recommendation system uses the technique of *collaborative filtering*. 
The main idea in this technique is to use similarities between users and 
similarities between items (movies, in our case) simultaneously to provide 
recommendations. Items are recommended (filtering) to a given user based on 
the interests of similar users (collaborating). 

The work was completed in a Jupyter Notebook, included in this repository.
The following steps are carried out in the notebook:
* The data is explored. 

* The dataset is split into training and test sets.

* A cross-validator is used to determine optimal hyperparameters. The best
model is selected.

* The best model is evaluated by comparing it with the baseline model.

* Given ratings supplied by a user, immediate recommendations are made,
without retraining the entire model.

**Main tools and packages used for the project:** 
[Jupyter Notebook](http://jupyter.org), 
[Apache Spark](http://spark.apache.org),
[NumPy](http://numpy.org), 
[pandas](http://pandas.pydata.org), 
[Matplotlib](http://matplotlib.org), 
[seaborn](http://seaborn.pydata.org), 
[Flask](http://palletsprojects.com/p/flask),
[jQuery](http://jquery.com), 
and 
[PHP](http://www.php.net).
