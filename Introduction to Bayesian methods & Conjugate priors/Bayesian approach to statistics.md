# Bayesian approach to statistics

the Frequentist one and the Bayesian one.So they differ in a lot of aspects.And the most important one is that the Frequentists treat the objective and
Bayesians treat it as subjective.
Imagine you have a coin and you toss it. What **Frequentist** would say that with probability one half it will end heads up and with probability
one half it will end tails up And you can do nothing about it.

However, what **Bayesian** would say is that if someone knew the initial velocity and all the initial parameters of the coin toss, you would be able to predict
the outcome of an experiment.And for this person the experiment would not be random.Another difference between Frequentists and Bayesians is how they treat
parameters in the data.

Bayesians is how they treat parameters in the data.
**Frequentists** would say that parameters are fixed and data is random.And they would want to find this optimal point.
However, **Bayesians** would say in a opposite way,that parameters are random and the data is fixed.And this actually makes sense.


![2020-03-31_180323](https://user-images.githubusercontent.com/46414243/78048388-f19c2280-7379-11ea-93d2-12202b7b5412.png)

When you train your model, you already know the data and it is not random anymore.However, there may be multiple good points and you would like to define a probability distribution over them.
Also **Bayesian** methods work for arbitrary number of letter points. While the Frequentist ones work only when the number of data points is much bigger than the number of parameters.
You may say that this is not a problem when we have the big data However, you may remember that for neural network we have millions of parameters However, the number of data points is only thousands.

![2020-03-31_210557](https://user-images.githubusercontent.com/46414243/78065338-70518980-7393-11ea-88d6-a0af50eb00ef.png)

Another difference is how **Frequentists** and Bayesians train their models.The Frequentists train using Maximum Likelihood Principle,that is they try to find the parameters theta that maximize the likelihood the probability of their data given parameters.

![2020-03-31_211302](https://user-images.githubusercontent.com/46414243/78066084-9a577b80-7394-11ea-81a3-fb7eb432d913.png)

However, what Bayesians will try to do is they would try to compute the posterior,the probability of the parameters given the data.And they would try to do this
using the Bayes formula.And this will give us a lot of interesting aspects.

![2020-03-31_211310](https://user-images.githubusercontent.com/46414243/78066648-a2fc8180-7395-11ea-97f0-ace01bfcce03.png)

It will compute the posterior distribution, in this case for the training data set, the x train and y train using the Bayes formula.We can compute the prediction,the probability of the new point y test given the training data set.This can be done using
marginalization principle theta times the probability of theta given the training set. And we'll have estimated it using the training procedure.


![2020-03-31_212116](https://user-images.githubusercontent.com/46414243/78066611-9415cf00-7395-11ea-9830-1247acff23f7.png)

This formula can also lead to regularization. We can treat the prior on theta as a regularizer.Imagine if you want to estimate the probability that your coin will land heads up.You already know that most of the coins land heads up with probability 0.5 and so
you can use the following prior, because we'll say that most of the coins are fair.
However, if you know that for your experiment the probability of heads can either be fair, that is 0.5 or bias towards heads, that is greater than 0.5, you could
use for example the following prior.
![2020-03-31_212605](https://user-images.githubusercontent.com/46414243/78067525-29fe2980-7397-11ea-8de2-7b0561b4b836.png)

Also Bayesian methods are really good for online learning.Imagine that you have data that comes in with some small portions.Then what you could do, you could
use it to update your parameters and Let's see it closer.The new posterior, the probability of theta indexed by k,equals to the posterior that we get after observing data point xk.
can use probability of theta indexed by k-1.

![2020-03-31_213035](https://user-images.githubusercontent.com/46414243/78067483-1783f000-7397-11ea-8fc5-786f20a14d0a.png)

Imagine you want to estimate some parameter theta.And here's your prior.Then you get for example ten points and you update it using the base formula.
And here's what you get.
The variance of the distribution is much less. And also you see that the mean has changed.And as you get more and more points, for example, here you can see for 20 points,
and 30 points, your estimation becomes more and more precise. And so you can predict the true value of the parameters very well.




![2020-03-31_213723](https://user-images.githubusercontent.com/46414243/78067916-d6401000-7397-11ea-8e7f-d463d485c1e0.png)











