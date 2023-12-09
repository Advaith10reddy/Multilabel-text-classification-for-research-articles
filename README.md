# Multilabel Text Classification with MLkNN
This repository contains Python code for performing multilabel text classification using the MLkNN (Multi-label k-Nearest Neighbors) algorithm. The code utilizes the scikit-multilearn library for MLkNN implementation and scikit-learn for preprocessing and evaluation.

## Prerequisites
Make sure you have the following dependencies installed:

pandas

numpy

scikit-learn

nltk

scikit-multilearn


## Install the required packages using the following command:
~~~
pip install pandas numpy scikit-learn nltk scikit-multilearn
~~~

## To prevent the following , update a single line in the skmultilearn package.

~~~
 error: TypeError: __init__() takes 1 positional argument but 2 were given
~~~

## In skmultilearn package


C:\Users\dudel\anaconda3\envs\unpr_fp_env_pd\Lib\site-packages\skmultilearn\adapt\mlknn.py

Specifically, old line 165:

~~~
self.knn_ = NearestNeighbors(self.k).fit(X)

~~~
should be updated to:
~~~
self.knn_ = NearestNeighbors(n_neighbors=self.k).fit(X)
~~~
