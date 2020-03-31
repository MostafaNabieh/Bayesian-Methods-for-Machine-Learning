## Think bayesian & Statistics review
Imagine you are running through a park and you see another man running.And you ask yourself, why is he running?
And you come up with four different explanations 
1. First, he is in a hurry.
2. Second, he is doing some sports.
3. Third, he always runs.
4. And fourth, he saw a dragon.

you will Three Principles, Principle 1, use prior knowledge.
From our previous experience we know that dragons do no exist. And so, we can exclude fourth option from next consideration.


Principle 2, choose answer that explains observations the most. Imagine you saw that he is not wearing a sports suit
In this case, it´s very unlikely that he´s doing sports, and so we can exclude number two.

Principle 3, avoid making extra assumptions. 
From the last two options, the third option, does he always runs makes a lot of extra assumptions and so should exclude it This principle is also known as Occam's Razor And finally, we are left with only one case, that he is in a hurry

![2020-03-31_163032](https://user-images.githubusercontent.com/46414243/78038343-08884800-736d-11ea-9066-cc7b32c3544b.png)

1. Principle 1, use prior knowledge.
2. Principle 2, choose answer that explains observations the most. Imagine you saw that he is not wearing a sports suit
3. Principle 3, avoid making extra assumptions. 

![2020-03-31_164102](https://user-images.githubusercontent.com/46414243/78039457-6e290400-736e-11ea-91a6-e99228e3611e.png)

### Before we continue, let's review some
basic principles from probability theory
The discrete for random variables can have either finite number of values that can take, as for example, for a dice. 
Or infinite, if you count the number of times that some certain event happened. An example of continuous random variable
would be at tomorrow's temperature.

![2020-03-31_164313](https://user-images.githubusercontent.com/46414243/78039878-f4dde100-736e-11ea-915a-bc5e66fbf62c.png)

the probability mass function.It maps a number for each point that refers to the probability. For example, in this case, 
which produces in 0.2. The 0.3 with probability 0.5 and so on with probability 0.3 and other points with probability 0 .
Also note that these points sum up to 1 . 

![2020-03-31_171641](https://user-images.githubusercontent.com/46414243/78043318-7d5e8080-7373-11ea-9c37-4075d21fc09b.png)

Or infinite, if you count the number of times that some certain event happened. An example of continuous random variable
would be at tomorrow's temperature. The most convenient way to find the discrete distribution is to call the probability mass function.

![2020-03-31_171654](https://user-images.githubusercontent.com/46414243/78044919-97995e00-7375-11ea-8cb5-76417238630c.png)

The two run variables are considered independent if their joint probability,The most convenient way to define continuous distributions is called a probability density function .We will also need a notion of independence. The two run variables are considered independent if their joint probability, that is, a probability of X and Y equals to the product of their marginals.that is, a probability of X and Y, equals to the product of their marginals So it will be a probability of X times a probability of Y.

![2020-03-31_172737](https://user-images.githubusercontent.com/46414243/78044413-f01c2b80-7374-11ea-9dc1-04c868f033da.png)

Let's see an example.Imagine that you have a deck of 52 cards and you take, randomly, 2 cards from it. And the first random variable would be the picture that is drawn on the first card and second would be the picture that is drawn on the second card. Those kind of variables are dependent since it is impossible to take one card two times. Another example is throwing two coins independently.

![2020-03-31_173508](https://user-images.githubusercontent.com/46414243/78045247-024a9980-7376-11ea-805b-ff5fdb863527.png)

Here the probability that the first coin will land heads up and the second would land tails up equals to the product of the two probabilities.these random variables are independent.

![2020-03-31_173737](https://user-images.githubusercontent.com/46414243/78045550-62414000-7376-11ea-82ca-b611b055d04a.png)

The last thing we'll need is a conditional probability. We want to answer a question, what is the probability of X given that
something that is called Y happened. It is given by the formula that you can see on the slide.It is the probability of X given Y equals
to the joint probability P of X and Y over the marginal probability P of Y.

![2020-03-31_174018](https://user-images.githubusercontent.com/46414243/78045843-b64c2480-7376-11ea-8225-22da1a1911aa.png)

Let's consider an example. Imagine you are a student and you want to pass some course.It has two exams in it, a midterm and the final.
The probability that the student will pass a midterm is 0.4 and the probability that the student will pass a midterm and the final 0.25.
If you want to find the probability that you will pass the final, given that you already passed the midterm, you can apply the formula from the previous slide. And this will give you a value around 60%.

![2020-03-31_174345](https://user-images.githubusercontent.com/46414243/78046326-53a75880-7377-11ea-9ada-edd952e487e8.png)

We'll need two tricks to deal with formulas.The first is called the chain rule.We can derive it from the definition of the conditional probability.
That is, the joint probability of X and Y equals to the product of X given Y and the probability of Y.By induction, we can prove the same formula for three variables.It will be the probability of X, Y, and Z equals to probability of X given Y and Z, the probability of Y given Z, and finally probability of Z.
And in a similar way, we can obtain the formula for the arbitrary number of points.So this would be the probability of the current point, given all its previous points.

![2020-03-31_175008](https://user-images.githubusercontent.com/46414243/78046966-18f1f000-7378-11ea-8e3b-08b4f758e63f.png)

The last rule is called the sum rule.That is, if you want to find out the marginal distribution p(X), and you know only the joint
probability that p(X,Y), you can integrate out the random variable Y, as it is given on the formula. 

![2020-03-31_175953](https://user-images.githubusercontent.com/46414243/78048045-72a6ea00-7379-11ea-96a7-9cb0cb38b5f7.png)

### And finally, the most important formula for this course, the Bayes theorem.
We want to find out the probability of theta given X,where theta are the parameters of our model. For example, we have a neural network and those are its parameters.And then we have X.Those are the observations, for example, the images that you are dealing with.
From the definition of the conditional probability, we can say that it is a ratio between the joint probability and the marginal probability, P(X). 
And also we apply the chain rule, we'll get the following formula. It will be the probability of X given theta, times the probability of
theta over probability of X. This formula is so important that each of its components has its own name. The probability of theta
is called a prior,it shows us what prior knowledge we know about the parameters. For example, you can know that some parameters are distributed at around 0. The term probability of X given theta is called a likelihood, and it shows how well the parameters
explain our data The thing that we get, the probability of theta given X, is called a posterior, and it is the probability of the parameters after we observe the data. And finally the term in the denominator is called evidence

![2020-03-31_180323](https://user-images.githubusercontent.com/46414243/78048388-f19c2280-7379-11ea-93d2-12202b7b5412.png)
