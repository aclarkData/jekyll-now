---
published: True
---
## Backpropagation Easily Explained

With the recent buzz in the deep learning research community over the efficacy and
future of [backpropagation](https://www.quantamagazine.org/new-theory-cracks-open-the-black-box-of-deep-learning-20170921/),
I thought this would be a good time to give an intuitive explanation for what
backpropagation is and how it works.

First off, what is backpropagation and why is it needed? Assuming that we have a model that takes
an input *x* and predicts an output, *y*, to make our model accurate, we train it by showing the machine
example inputs and outputs and optimize an error function (essentially a function that calculates
how far the predicted *y*, *yhat* is from the real *y*, i.e. if we predict 2, but the output is 1, we would have an "error"
of 1 (i'm taking numerous liberties on the mathematical exactness for illustration purposes)).

Backpropagation is the process we use to update the model coefficients (for the linear equation *y = mx + b*,
m and b are coefficients) to better fit the data. Backpropagation is a type of gradient descent used in neural networks, where each layer has an input, weight[s] and an activation function (basically a function that takes the input x weight[s] as an input and decides whether or not to "fire" the neuron and what value to return). As in regular gradient descent,
we take the rate of change for each of the model coefficients (the partial derivative), remember *m* and *b*,
and multiply this rate of change times a very small "step", let's say for illustration 0.001, times the weight (you could think of the weight in this instance as being the *x* of the *mx+b*) times the current model coefficient (we would perform this twice, once for m and once for b). We will then rerun the model and see if the results are better. If they are worse, we will move in the other direction, for instance, we recalculate the derivatives x step x weight x coefficients value and add a negative to the front. If this result is better the next time the model is run, we continue in this same direction (with the negative) until we can't get any more accurate (we would probably overshoot and change directions to get back to the lowest error). So essentially, backpropagation is the process of adjusting the weights of the model by small amounts to minimize the error. The complexity occurs when we have a deep neural network (one with many layers), with a lot of input (say 256, one input for each image pixel) that has a set of weights at each layer. This same process we discussed above plays out, but on a large scale in a neural network. A lot of people who have a reasonably good grasp of gradient descent get confused with backpropagation, thinking it is qualitatively different than gradient descent, when in fact the process is the same, except the output error is used to update multiple layers instead of the single "layer" of our example linear model.

Hopefully this intuitive guide has proved useful. Eventually, as time allows, I will create two more posts on backpropagation:
* Backpropagation in code 
* Backpropagation: the math.  

Andrew
