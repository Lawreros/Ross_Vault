## Week 1:
Video #1:
- ReLU function
- Layer
- neural network

Video #2: Supervised Learning with Neural Networks
- convolutional neural network
- recurring neural network (RNN)
- structured data
		- Clearly defined parameters (think a table of numbers)
- unstructured data
		- Image, audio, text (so stuff where you don't really know what you are going to be given)

Video #3: Why is Deep Learning taking off?
- Scale drives the deep learning process. The more data you have, the better deep learning models perform. Traditional learning algorithms, such as SVM or logistic regression, tend to plateau after reaching a certain size of data.
- The bigger/deeper the neural net, the more it improves for larger and larger datasets (compared to smaller NN)

Video #4: About this Course


## Week 2:
Video #1: Binary Classification
Binary Classification is the process of taking in an input vector and outputting a binary value which determines if the input falls into a given category (using 1 or 0).

Notation for this course:
Training input data will be denoted as $(x,y)$ where $n_x$ is the number of features and $$x \in \mathbb{R}^{n_x}, y\in \{0,1\}$$
The $m$ training examples are treated as a set: $\{(x^{(1)},y^{(1)}),(x^{(2)},y^{(2)}),...,(x^{(m)},y^{(m)})\}$
The collection of all the input features is denoted as:
$$X = \begin{bmatrix}| & | & ... & |\\
x^{(1)} & x^{(2)} & ... & x^{(m)} \\
| & | & ... & |
\end{bmatrix} \in M_n(\mathbb{R}^{n_x \times m})$$ 
and the corresponding labels are denoted as $$Y = [y^{(1)}, y^{(2)},...,y^{(m)}]$$

Video #2: Logistic Regression
Logistic Regression
Sigmoid Function

Video #3: Logistic Regression Cost Function


Video #4: Gradient Descent
Gradient Descent
$$ w := w-\alpha \frac{\delta J(w,b)}{(\delta w)}$$
$$b := b- \alpha \frac{\delta J(w,b)}{\delta b}$$


Video #5: Derivatives
Video #6: More Derivative Examples

Video #7: Computation Graph
The computation graph is just a way of representing (using boxes and arrows) how the input parameters are fed into and utilized by a function.

Video #8: Derivatives with a computation graph
Forward calculation gives you cost function/final output
Backward calculation gives you derivatives

Video #9: Logistic Regression Gradient Descent
Walks through the manual calculation of the forward and backward update of a Logistic Regression learning algorithm

Video #10: Gradient Descent on m Examples
How the gradient descent algorithm works when you are using more than one training example at a time
Vectorization (getting rid of `for` loops)

### Python Videos

Video #1: Vectorization
The use of vectors to do a lot of calculations faster (instead of multiplying each entry in to vectors and summing the all together)


Video #2: More Vectorization Examples
The usefulness of python programs like numpy in doing vector and matrix calculations.
`math.exp(v[i])`

Video #3: Vectorizing Logistic Regression
`np.dot(w.T,X)+b` where $b \in \mathbb{R}$ is called "broadcasting"

Video #4: Vectorizing Logistic Regression's Gradient Output
Going through the learning process of performing logistic regression using as much vectorization as possible.

Video #5: Broadcasting in Python
The various tips and tricks of messing around with numpy arrays

Video #6: A Note on Python/Numpy Vectors
Discusses in greater detail about the potential bugs that may occur when using numpy with vectors and matrices.
- rank 1 arrays should be avoided. `np.random.rand(5,1)` instead of `np.random.rand(5)`

Video #7: Quick tour of Jupyter/iPython Notebooks
Self-explanatory....

Video #8: Explanation of Logistic Regression Cost Function

## Week 3
Video #1: Neural Networks Overview
- Notes on the notation that will be used this week
- round brackets are entry of vector $x^{(1)}$
- square brackets are all entries in layer $W^{[1]}$

Video #2: Neural Network Representation
- "Input layer"
- "Hidden layer"
- "output layer"
- Do not count the input layer when saying something is a "N-layer" neural network

Video #3: Computing a Neural Network's Output
- Each node of a NN diagram (i.e. the circles in each layer) actually consist of two steps, the $w^Tx+b$ and the $\sigma(z)$
- How to vectorize a layer of the NN: 
$$ W^{[1]}x+b^{[1]}=\begin{bmatrix} - & w_1^{[1]T} & - \\
-& w_2^{[1]T} & -\\
-& w_3^{[1]T} & -\\
-& w_4^{[1]T} & - \end{bmatrix} \begin{bmatrix}x_1 \\ x_2 \\ x_3\\ \end{bmatrix} +\begin{bmatrix}b_1^{[1]} \\ b_2^{[1]} \\ b_3^{[1]}\\ b_4^{[1]} \end{bmatrix} = \begin{bmatrix}w_1^{[1]T} x + b_1^{[1]} \\ w_1^{[1]T}x +b_2^{[1]}\\ w_3^{[1]T}x+b_3^{[1]}\\ w_4^{[1]T}x+b_4^{[1]} \end{bmatrix} = \begin{bmatrix}z_1^{[1]} \\ z_2^{[1]} \\ z_3^{[1]}\\ z_4^{[1]} \end{bmatrix} = z^{[1]}$$
and 
$$a^{[1]} = \begin{bmatrix}a_1^{[1]} \\ a_2^{[1]} \\ a_3^{[1]}\\ a_4^{[1]} \end{bmatrix} = \sigma(z^{[1]})$$

Video #4: Vectorizing Across Multiple Examples
- Same as previous video, just make $X$ have each column be a different vector $x$


Video #5: Explanation for Vectorized Implementation


Video #6: Activation Functions
- hyperbolic tangent function
- ReLu funtion
- Leaky ReLu
- Discusses how sigmoid activation function shouldn't really be used except for last layer

Video #7: Why do you need Non-Linear Activation Functions?
- Because the composition of two linear functions is itself a linear function. Thus, if you had only linear layers, it would be as if you just had one linear layer as all the weights could be simplified down.
- Sometimes want to use linear layer for the output layer, like with predicting housing prices, so that your outputs are numbers outside of the range 0-1

Video #8: Derivatives of Activation Functions
- List of the derivatives for each activation function we have covered so far

Video #9: Gradient Descent for Neural Networks


Video #10: Backpropagation Intuition


Video #11: Random Initialization


## Week 4

Video #1: Deep L-layer Network
- L just denotes the number of layers in the network. Remember that the input layer is not counted.
- $n^{[l]}=$ number of units in layer $l$
- $n^{[0]}=n_x$, so the number of input features
- $a^{[L]} = \hat{y}$ i.e. the predicted output

Video #2: Forward Propagation in a Deep Network
- Vectorization of forward propagation of multiple layered network (exactly what you expect)

Video #3: Getting your Matrix Dimensions Right
- Just a video about checking the dimensions of you weight, bias, and layer matrices to make sure that they make sense

Video #4: Why Deep Representations?
- Example about how deep networks work (think what was covered in sparse with convolutional NN)

Video #5: Building Blocks of Deep Neural Networks
- 

Video #6: Forward and Backward Propagation
- Introduces the caching of intermediate $z$ outputs from layers during forward propagation for later use in backward propagation
- $dz^{[l]} = W^{[l+1]T}dz^{[l+1]}\times g^{[l]}(z^{[l]})$

Video #7: Parameters vs. Hyperparameters
- hyperparameters:
		- Learning rate
		- number of iterations for gradient descent
		- number of layers
		- number of nodes per layer
		- activation function

Video #8: What does this have to do with the brain?


