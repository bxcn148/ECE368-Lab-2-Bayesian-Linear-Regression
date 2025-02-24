Download link :https://programming.engineering/product/ece368-lab-2-bayesian-linear-regression/


# ECE368-Lab-2-Bayesian-Linear-Regression
ECE368: Lab 2: Bayesian Linear Regression
In this lab, we use Bayesian regression to t a linear model. Consider a linear model of the form

z = a1x + a0 + w;

(1)

where x is the scale input variable, and a = (a0; a1)T is the vector-valued parameter with unknown entries a0, a1, and w is the additive Gaussian noise:

w N (0; 2);

(2)

where 2 is a known parameter.

Suppose that we have access to a training data set containing N samples fx1; z1 g; fx2; z2g; : : : ; fxN ; zN g. We aim to estimate the parameter a by nding its posterior distribution. When the training nishes, we make predictions based on new inputs. We consider a Bayesian approach, which models the parameter a as a zero mean isotropic Gaussian random vector whose probability distribution is expressed as

p (a) = N

0

;

0

;

(3)

0

0

where is a known hyperparameter.

Download reg.zip under Files/Labs/Lab2 Part1/ on Quercus and unzip the le. File training.txt contains the training data: the rst column is the inputs; the second column is the targets. The training data is generated from z = 0:5x 0:1 +w. Please answer the questions below and complete regression.py. File util.py contains a few useful functions.

Questions

Express the posterior distribution p(ajx1; z1; : : : ; xN ; zN ) using 2; , x1; z1; x2; z2; : : : ; xN ; zN .

Let 2 = 0:1 and = 1. Based on the posterior distribution obtained in the last question, draw four

contour plots corresponding to p(a), p(ajx1; z1), p(ajx1; z1; : : : ; x5; z5), and p(ajx1; z1; : : : ; x100; z100). In all contour plots, the x-axis represents a0, and the y-axis represents a1. The range is set as [ 1; 1] [ 1; 1]. In each gure, also draw the true value of a, which corresponds to the point ( 0:1; 0:5).

Suppose that there is a new input x, for which we want to predict the target value z. Write down the distribution of the prediction z, i.e., p(zjx; x1; z1; : : : ; xN ; zN ).

4. Let 2 = 0:1 and = 1. Suppose that the set of the new inputs is f 4; 3:8; 3:6; : : : ; 0; : : : ; 3:6; 3:8; 4g.

Plot three gures corresponding to the following three cases:

The predictions are based on one training sample, i.e., based on p(zjx; x1; z1).

The predictions are based on 5 training samples, i.e., based on p(zjx; x1; z1; : : : ; x5; z5).

The predictions are based on 100 training samples, i.e., based on p(zjx; x1; z1; : : : ; x100; z100).

In all gures, the x-axis is the input, the y-axis is the target, and the range is set as [ 4; 4] [ 4; 4]. Each gure should contain three components: 1) the new inputs and the predicted targets; 2) a vertical interval at each predicted target, indicating the range within one standard deviation; 3) the training sample(s) that are used for the prediction. Use plt.errorbar for 1) and 2); use plt.scatter for 3).

References: C. M. Bishop, Pattern Recognition and Machine Learning, Springer New York, 2006, pp. 152{

& K. Murphy, Machine Learning: A Probabilistic Approach, MIT Press, 2012, pp. 231{234.
