# how to define a probabilistic model

The most convenient way to do this is called the Bayesian Network. It is a graph.Its nodes are random variables and edges are direct impact.
For example, here we have two random variables,rain and the fact that the grass is wet.And these edge shows as if there is rain,if it's raining, then the grass will be wet for sure.

We can see a more complex graph.For example, here we added another random variable called sprinkler,and the grass maybe wet either because the sprinkler is working or because it is raining.
and the grass maybe wet either because the sprinkler is working or because it is raining.Also the sprinkler will not work if there is rain. From the graph, we can write down the probabilistic model.


![2020-03-31_215454](https://user-images.githubusercontent.com/46414243/78069393-51a2c100-739a-11ea-88a8-1796c4b1c674.png)

The probabilistic model is a joint probability over all random variables. The joint probability over all variables equals to the product for each variable, is probability given all the parents.
On this graph, for example,Let's try to write down the probabilistic model for this graph.

![2020-03-31_220100](https://user-images.githubusercontent.com/46414243/78070122-882d0b80-739b-11ea-927c-a027bf2c4903.png)

So the joint probability of sprinkler,rain, and the grass equals to the product of two terms.The first one is the probability of grass is worse given the sprinkler and the rain.Those are the parents of this node.
Next, multiplier is the probability of the sprinkler given the rain.The rain is the only parent of this node.And finally, we write down the probability of the rain.
Since this node doesn't have any parents,we just write down the probability of the rain.And this is our final model.

![2020-03-31_220529](https://user-images.githubusercontent.com/46414243/78070251-c0cce500-739b-11ea-8e33-47012416b0e9.png)

For example, you all know the Naive Bayes classifier. It's graphical model looks as follows.We have a class,C that directly impacts the values of the features,that is for different classes.
The distribution of the features may be different.And the joint distribution can be written using the following formula.It is the probability of the class times the product over all features,the probability of the current feature given the class.
However, this notation is a bit interesting since we have a lot of equal sub-graphs.A bit more convenient way to write down this graph is called a plate notation.

![2020-03-31_220926](https://user-images.githubusercontent.com/46414243/78070563-4e103980-739c-11ea-82fc-a157d92d5214.png)

It is written as follows.So we have a random variable that corresponds to the class,that directly impacts the features.And this works around this random variable with a number ofrepetitions such that we have to repeat this sub-graphthat is contained inside this box and times.And so this is exactly Kuhn's graphical model,

![2020-03-31_221356](https://user-images.githubusercontent.com/46414243/78070968-f2927b80-739c-11ea-88d7-e9e89957ace7.png)
