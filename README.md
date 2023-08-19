# Student-Academic-Performance-From-Scratch

👋 Welcome to my GitHub project!

## Purpose
- The purpose of this project was to use the structure of neural network from scratch (Neural Networks from Scratch) in order to predict the acceptance or rejection of students according to a set of their characteristics during an academic semester, which then was also done using tensorflow.</br >
More details about the dataset can be observed through [Student's Academic Performance](https://www.kaggle.com/datasets/aljarah/xAPI-Edu-Data).

## Description
Here's a summary of the general process involved in this project: </br>

1️⃣ Neural Network Implementation:
   - We start by feeding the input data into the neural network.
   - Data flows through the network layers until the final output is generated.
   - Once the output is ready, we can calculate the error.

2️⃣ Training of the Implemented Model:
   - During this phase, we train the neural network model.
   - The training process involves adjusting the parameters (weights and biases) based on the calculated error.
   - The adjustment is done by subtracting the derivative of the error from the respective parameter.
   - The process of feeding data, calculating error, and updating parameters is repeated iteratively.

3️⃣ Evaluation of the Trained Model:
   - After training the model, we evaluate its performance.
   - The evaluation phase involves calculating the accuracy and loss of the model on evaluation data.

Let's dive deeper into each phase: </br>

1️⃣ Neural Network Implementation:
   - Here, we will implement a neural network for two-class classification (accept or reject).
   - The implementation consists of four main steps.

   - Step 1: Setting weights and activation threshold:
     - We randomly initialize the weights (W) in the weight matrix and the activation threshold (b).

   - Step 2: Forward Propagation:
     - We provide input data (X) to the network.
     - The network produces an output (A).
     - We compare the network's output (A) with the desired output (Y) to calculate the error (E).

   - Step 3: Backward Propagation:
     - The goal of this step is to minimize the error (E).
     - We update the weights and biases (𝜕𝑊, 𝜕𝑏) based on the error.

   - Step 4: Combining the Previous Steps and Building the Final Algorithm:
     - We combine the functions implemented in the previous steps to create the final model.
     - The final model performs forward propagation, computes the values of A and E, performs backward propagation, and updates the values of W and b.
     - This process is repeated k times.

2️⃣ Training of the Implemented Model:
   - In this phase, we apply the algorithm implemented in the previous section to the available training data.
   - We train the model using a recommended value for k (e.g., 1000) and learning rate (α) value (e.g., 0.1).
   - Additionally, we calculate the accuracy and loss on the training data for each iteration (k).

3️⃣ Evaluation of the Trained Model:
   - After completing the training phase, we evaluate the performance of the trained model.
   - We calculate the accuracy and loss of the model on the evaluation data.

In order to better understand the issue, the following figure is presented as an example, which has two layers (input layer and output layer), a threshold and two inputs (x1 and x2) and the output predicted by the network (A). Also, the sigmoid activation function is used for the output layer. </br>

<div align="center"><img src="https://github.com/HosnawHb/Student-Academic-Performance-From-Scratch/blob/main/NN.png?raw=true"width="60%"/></div> </br >

### Formulas:
  - $$𝑍=𝑊^𝑇 𝑋+𝑏$$
  $$𝐴=𝑠𝑖𝑔𝑚𝑜𝑖𝑑(𝑍)$$
  $$𝐸=-\frac{1}{n}\sum_{i=1}^n (𝑦_𝑖 log(𝑎_𝑖)+(1−𝑦_𝑖)log(1−𝑎_𝑖))$$
  $$\frac{𝜕𝐸}{𝜕𝑊}=\frac{1}{n}𝑋 (𝐴−𝑌)^𝑇$$
  $$\frac{𝜕𝐸}{𝜕b}=\frac{1}{n} \sum_{i=1}^n (𝑎_𝑖−𝑦_𝑖)$$
  $$𝑊=𝑊−𝛼\frac{𝜕𝐸}{𝜕𝑊}$$
  $$𝑏=𝑏−𝛼\frac{𝜕𝐸}{𝜕b}$$


Please refer to the code in the repository for a step-by-step guide on implementing the neural network, training the model, and evaluating its performance.








