## Movie Recommendation System

**Manish Jaiswal**

### Executive summary

One of the critical problem in today's exploding e-commerce and streaming services landscape is around how to keep customer engaged on the respective platform. Engaging customer means, increased sales, customer loyalty, customer satisfaction and reducing churn.

Movie recommendation system, intends to solve such problem for a streaming service by enabling platform to provide movie recommendations for a user based on user's viewing and rating patterns and similarity with other users patterns.

### Rationale
**Why should anyone care about this question?**

As described above, a good recommendation system / model can play crucial role in business growth. We can apply recommendation models in varying areas like e-commerce, retail, media, banking , utilities etc.

With such models in place, we can personalize customer's experiences and enable better customer engagement.

### Research Question
**What are you trying to answer?**

Using the recommendation models learnt during the course, I plan to answer following questions
1. Given a user, what are the top 10 movie recommendations
2. Given a user, what are the top 3 Genre recommendations
3. Given a user, what are the top 5 users similar to the user.
4. Given a movie, what are the top 5 movies similar to it.
5. How do the different model compare against each other w.r.t training time, accuracy, precision, recall
6. Identify best parameters for each model being tested.

### Data Sources
**What data will you use to answer you question?**
I will be using MovieLens dataset below
https://files.grouplens.org/datasets/movielens/ml-100k.zip

### Methodology
**What methods are you using to answer the question?**

For questions related to similarity, we will utilize 
**distance based recommendations**.

Then we will utilize following models exposed by Surprise package.
1. KNNBasic
2. SVD
3. CoClustering

**As next steps**, I want to apply neural network techniques for answering questions i am going for.

### Results
What did your research find?

Below is the performance comparison on different models executed

| model        | Default Fit Time | Default RMSE | CrossCV Fit Time | CrossCV RMSE | GridSearchCV Fit Time | GridSearchCV RMSE | GridSearchCV Best Params                                              |
| ------------ | ---------------- | ------------ | ---------------- | ------------ | --------------------- | ----------------- | --------------------------------------------------------------------- |
| KNNBasic     | 0.115443945      | 0.726238927  | 0.075817204      | 0.946783728  | 77.426934             | 0.953747264       | {'k': 20, 'sim\_options': {'name': 'msd', 'user\_based': True}}       |
| SVD          | 5.296315908      | 0.641187613  | 4.667572451      | 0.875052874  | 205.6373751           | 0.869232585       | {'n\_factors': 2, 'n\_epochs': 20, 'lr\_all': 0.01, 'reg\_all': 0.04} |
| CoClustering | 1.420558929      | 0.826301644  | 1.442201614      | 0.947971527  | 296.9580288           | 0.954353775       | {'n\_epochs': 150, 'n\_cltr\_u': 5}                                   |

### Outline of project

- [Distance Based Similarity User n Movies](https://github.com/manish237/AIMLCapstone/blob/main/Capstone-DistanceBased.ipynb)
- [Movie Recommendation using KNNBasic](https://github.com/manish237/AIMLCapstone/blob/main/Capstone-KNN.ipynb)
- [Movie Recommendation using SVD](https://github.com/manish237/AIMLCapstone/blob/main/Capstone-SVD.ipynb)
- [Movie Recommendation using CoClustering](https://github.com/manish237/AIMLCapstone/blob/main/Capstone-coclustering.ipynb)


### Contact and Further Information
Email: manish23@gmail.com