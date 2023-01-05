name : Leaky ReLU
tags : 
backlinks : 
source : https://paperswithcode.com/method/leaky-relu#:~:text=Leaky%20Rectified%20Linear%20Unit%2C%20or,is%20not%20learnt%20during%20training, https://pytorch.org/docs/stable/generated/torch.nn.LeakyReLU.html

###### Content:
The Leak Rectified Linear Unit, or Leaky ReLU, is a type of [[activation function]] based on a [[ReLU]], but with a small slope for negative values instead of a flat slope. This can be written as: $$f(x) = max(0,x)+a*min(0,x)$$ where $a\in \mathbb{R}$ is the specified slope when $x <0$.

![[Pasted image 20221119202723.png]]

###### Properties:
- This type of [[activation function]] is popular in tasks which may suffer from [[sparse gradient]]s, for example training [[generative adversarial network]]s
- The gradient for negative values is a small value that makes learning of model parameters time-consuming
- It has theoretical advantage over [[ReLU]] due to being influenced by $x$ at all values, not just when $x>0$, and thus may be making more "complete" use of the information contained in $x$.
	- *"Their are other alternatives, but both practitioners and researchers have generally found insufficient benefit to justify using anything other than ReLU."*

###### Additional Thoughts:
