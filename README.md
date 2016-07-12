# NeuralNetPlayground


A MATLAB implementation of the Neural Networks Playground.


## Description

Inspired by the Neural Networks Playground interface readily
available online, this is a MATLAB implementation of the same Neural Network
interface for using Artificial Neural Networks for regression and
classification of highly non-linear data.

The interface uses the *HG1* graphics system in order to be compatible with
older versions of MATLAB.  A secondary purpose of this project is to write a
vectorized implementation of training Artificial Neural Networks with
Stochastic Gradient Descent as a means of education and to demonstrate the
power of MATLAB and matrices.

The goal for this framework is given randomly generated training and test data
that fall into two classes that conform to certain shapes or specifications,
and given the configuration of a neural network, the goal is to perform either
regression or binary classification of this data and interactively show the
results to the user, specifically a classification or regression map of the
data, as well as numerical performance measures such as the training and test
loss and their values plotted on a performance curve over each iteration.
The architecture of the neural network is highly configurable so the results
for each change in the architecture can be seen immediately.

There are two files that accompany this repo:

- `NeuralNetApp.m`: The GUI that creates the interface as seen on TensorFlow
  Neural Networks Playground but is done completely with MATLAB GUI elements
  and widgets.
- `NeuralNet2.m`: The class that performs the Neural Network training via
  Stochastic Gradient Descent. This is used by the `NeuralNetApp.m` app.


## Compatible Versions

Debugged and tested for MATLAB R2009b or newer.

This code can only be run on versions from R2009b and onwards due to the
syntax for discarding output variables from functions via (`~`).  If you wish
to use this code for older versions (without guaranteeing compatibility), you
will need to replace all instances of discarding output variables with dummy
variables but you'll be subject to a variety of `mlint` errors.  This effort
has not been done on our part as there is very little gain to go to even older
versions and so if you desire to run this code on older versions, you will
have to do so yourself.


## Neural Network App

Ensure that both files `NeuralNetApp.m` and `NeuralNet2.m` are in the same
directory.  In the MATLAB Command Window, simply run the `NeuralNetApp.m` file
within this directory. Assuming you are working in the directory of where you
stored, type in the following and press ENTER:

``` matlab
>> NeuralNetApp
```

If you want to be explicit, you can use `run` and provide the path to where
this file is located on your system:

``` matlab
>> run(fullfile('path', 'to', 'the', 'NeuralNetApp.m'));
```



## Neural Network Class

The main engine before the training algorithm is seen in the `NeuralNet2.m`
file.  This is a custom class that was written and is well documented to allow
a MATLAB user to use it for their purposes in future code that they write.
You can type in `help NeuralNet2` in the command window where this file is
located on your system for a comprehensive overview on how to use this class.
