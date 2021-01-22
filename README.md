# Latent Factor Recommendation System
A Latent Factor Recommendation system that we can use to recommend movies to users.
It is a simple Implementation of Stochastic Gradient Descent algorithm to build a Latent Factor Recommendation system. Using PySpark would be a good idea, as the data is going to be huge, it would be easy to process the data in parallel across a cluster.
```ratings.csv``` is the matrix R. Each entry is a movie id, user id, and a rating that is an integer between 1 and 5. It has around 609 users and 9485 movies. As you can see, it is a small dataset I have used NumPy.

![RQP](https://github.com/DVD-99/Latent_Factor_Recommendation_System/blob/master/model.png)

We are given a matrix R of recommendations. The element R<sub>iu</sub> of this matrix corresponds to the rating given by user **u** to item **i**. The size of R is **m × n**, where **m** is the number of movies and **n** the number of users. Most of the elements of the matrix are unknown because each user can only rate a few movies. Our goal is to find two matrices, P and Q, such that R = QP<sup>T</sup>. The dimensions of Q are **m × k**, and the dimensions of P are **n × k**. k is a parameter of the algorithm.
