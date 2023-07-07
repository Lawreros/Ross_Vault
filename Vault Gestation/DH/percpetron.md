name : percpetron
tags : 
backlinks : 
source : https://towardsdatascience.com/what-is-a-perceptron-basics-of-neural-networks-c4cfea20c590, https://towardsdatascience.com/what-the-hell-is-perceptron-626217814f53, https://www.simplilearn.com/tutorials/deep-learning-tutorial/perceptron#:~:text=A%20Perceptron%20is%20a%20neural,value%20%E2%80%9Df(x)

###### Content:
A perceptron is a single layer [[neural network]], consisting of 4 parts:
1. An input layer
2. Weights and [[bias]]
3. A net sum
4. An [[activation function]] (in the image below it is a step function)

![[Pasted image 20230622155547.png]]

In other words, the perceptron is an algorithm for learning a [[binary classification]] is a function that maps its input $x \in \mathbb{R}^n$ to an output value $f(x)$: $$f(x) = \phi(w \cdot x+b)$$ where $w$ is the weights, $b$ is the [[bias]], and $\phi$ is the [[activation function]].
 

###### Properties:
- A perceptron is usually used to classify data into two parts. Therefore, it is also known as a "Linear Binary Classifier"
- A multi-layered perceptron model is similar to a single-layer perceptron model, only with more hidden layers

###### Additional Thoughts:
