wThe BCPNN is a local learning rule for networks, as compared to the backpropagation algorithm which are global.

**Idea**
The Two Layer BCPNN model consists of one input layer and one output layer. Each neuron in the output layer performs a simple transformation of the inputs: it calculates the weighted sum of inputs and adds a bias term.

The two layers of neurons are organized in a modular architecture of *hypercolumns* consisting of sub-units called **minicolumns**. The input space has as many hypercolumns as attributes in the dataset, capturing one attribute of the input space.
![[Pasted image 20230206091106.png]]


**Formulation**
Assume 
* a dataset $X$ consists of $d_1$ attributes (categorical variable), i.e. $X_k \in \{x_1, ... x_n\} n \in N$, 
* with a categorical output $Y \in \{y_1, ..., y_m\} m \in N$.
* and we wish to predict $P(Y|X)$ .
Then, Bayes theorem states the following about Y given the datapoint $X^{(i)}$:
$$P(y_j,X^{(i)})=\prod_{x_{kk'} \in X^(i)} \frac{P(x_{kk'}|y_j)P(Y_j)}{P(x_{kk'})}$$
Taking the logarithm yields, with the indicator variable $o_{kk'}$:
$$log \; P(y_j,X^{(i)})=\sum_{x_{kk'}} \frac{P(x_{kk'}|y_j)}{P(x_{kk'})}o_{kk'}+log \; P(Y_j)$$
We observe that this has a similar structure as the multi-layer perceptron architecture:
* $log \; P(y_j,X^{(i)})$ - the support 
* $\frac{P(x_{kk'}|y_j)}{P(x_{kk'})}$ - the weight between the $kk'^{th}$ unit in the input and the $j^{th}$ unit in the output,
* $log \; P(Y_j)$ - the bias of the $j^{th}$ unit in the output $b_j$.

**Learning**
[[_Regression with Bayesian Confidence Propagating Neural Networks]] have good explanations for incremental learning and other aspects.