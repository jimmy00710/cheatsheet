## WHY ACTIVATION FUNCTIONS-
Why do we need activation function in our neural network? Why can't we build a simple neural network without any activation function? <br>

So let us take a case where there is no activation function. In that scenario what will happen ? <br> 
So we will be multiplying weights with the input, add bias. Since we are not applying any activation function, we are just trying to separate the classes using a linear hyperplane. <br>
<b><strong>h(0) = X.W + b</strong></b>

And most of the data is not linear. <br>

If we perform simple linear operation i.e, multiply the input by weight, add bias term and sum them across all the inputs arriving in the neuron. In some cases, the output of the above values is very large. When this output is fed to the furthermore layers, the values become even larger, making things computationally uncontrollable. <br>

This is where activation function come into picture. It squashes the value real input number to a fixed intervals. i.e between -1 and 1. <br>

<img src="https://miro.medium.com/max/406/0*UTHoA1EPXsjbN6bI.png"><br>

### Different Types of Activation Function- 

#### Sigmoid - 
Sigmoid is a smooth function and is continuously differentiable. This is a non-linear function and it looks like S-shape. 
<b> The main reason to use the sigmoid function is that it squashes the input value between 0 and 1. </b>
The mathematical representation is as follows- <br> 
<b> Graph of sigmoid function </b>
<img src="https://miro.medium.com/max/485/1*BwZmaMBaVW8f8lBAQUoytw.png"> <br>

<b> Graph of sigmoid derivative</b> - 
<img src="https://miro.medium.com/max/700/1*3LdsKVac4UvK8912ORIPvQ.jpeg">

> Sigmoid function is easily differentiable and the values are dependent on x values. 
<img src="https://miro.medium.com/max/700/1*nJ8lh4DoR8bAfLNeGwKHQQ.jpeg">

##### Code Snippet - 
> def sigmoid(z):<br>
 return 1 / (1 + np.exp(-z))

 ##### Problems - 
Values obtained from sigmoid are not <b> zero centred</b>
We can easily face the issue of vanishing gradients and exploding gradients. 