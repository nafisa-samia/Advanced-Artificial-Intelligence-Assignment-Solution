# Advanced-Artificial-Intelligence-Assignment

## Exercises

## 1. Introduction to NN
---
Create a neural network for [American Sign Language alphabec](http://www.asl.gs/), using this dataset [Sign Language MNIST](https://www.kaggle.com/datamunge/sign-language-mnist) from [kaggle](https://www.kaggle.com/) which has the same format as the MNIST data.

**Objetives:**
- Explore and prepare image data for training and validation
- Create and compile a simple model for image classification
- Train an image classification model and observe the results

The model specifications are as follows:
- Dense input layer. 
- First hidden layer with **512 neurons** fully connected, use the `relu` activation function.
- Second hidden layer with **512 neurons** fully connected, use the `relu` activation function.
- Dense output layer with **neurons equal to the number of classes**, using the `softmax` activation function.

Use [categorical crossentropy](https://www.tensorflow.org/api_docs/python/tf/keras/losses/CategoricalCrossentropy) to reflect the fact that we want to fit into one of many categories, and measuring the accuracy of our model.

Training specifications:
- Use the model's `fit` method to train it for **20 epochs** using the training and validation images and labels

Discussion:
- What is observed in the training results and why does it happen?


## 2. NN Optimization
---

**Reminder**: The general methodology to build and compute our Neural Networks is to:

1. Create the baseline of the NN.
    - Create the model (sequential model)
    - Define the structure of your NN:
    - decide on the initialization of the weights
    - Add the layers
        - No. of input units
        - No. of hidden units
        - No. of layers
        - No. of output units
        - activation functions
    - Which optimizer are you using(for gradien descent use SGD)?
    - How are you calculating the Loss?
2. Compile the model
3. Return the model
4. Train your model
    - How many epochs?

5. Try re-running the previous example and investigate what happens when you change when you change:
    
    - No. iterations: 100, 500, 1000, 2000
    - No. Hidden units: 1, 2, 3, 4, 5, 10, 50
    - Change the learning rate
    - What happens if you change the activation function?
    - try adding new Layers

How to select what kind of tunnning does our model might need?
    
    1) Plot the training error and the dev/test error.
    2) Take a look at the Bias and Variance of the results
    3) Does your model have high bias?
        - Train a bigger network (more layers)
        - Train longer (more epochs)
        - Change the network architechture
    4) Does your model have high variance?
        - Get more data
        - Apply regulatization
        - Change the architechture



## 3. Deep Reinforcement Learning 
---


a) Linearly decaying learning rate

Depending on the current episode let the learning rate decay linearly.


b) Normalizing returns

Normalize the already computed returns that are used for the loss.

Hint: You might need to call these tensor functions: .mean(), .std()


c) Neural Network Architecture

Change the activation function or the size of the neural net.

e.g. add a hidden layer
e.g. change the number of units in a layer
e.g. use nn.LeakyReLU instead of nn.ReLU


d) Compare your results using Tensorboard.
Important: Change the run_id for each run!

e) Test another environment.

Classic Control Environemtns: https://gym.openai.com/envs/#classic_control

MountainCar-v0

Acrobot-v1

Pendulum-v0


