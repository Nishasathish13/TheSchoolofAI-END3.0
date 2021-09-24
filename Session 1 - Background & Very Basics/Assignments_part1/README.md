# ASSIGNMENT PART 1
## Assignment Part 1 consists of an .ipynb notebook along with required description


# ASSIGNMENT PART 2
## Assignment part 2 is a descriptive section describing the below concepts.

### 1. What is a neural network neuron?
![image](https://user-images.githubusercontent.com/75114179/134708427-63d880d9-66ad-48ff-a11b-428aa9cea105.png)
*Title: Neural network*

  Neurons also known as perceptrons are the basic fundamental unit of a Neural Network. In the above image, each of the circle we see represents a neuron. They are arranged in the form of layers, with the first layer taking in inputs and the last layer producing the output. The middle layers have no connections with the external world and hence are called hidden layers. Each neuron or perceptron in one layer is connected to every perceptron on the next layer. 
  
  Neurons are merely used to store values temporarily and the computational function (weights and activation fuction) lie outside these neurons.
  
### 2. What is the use of the learning rate?
### 3. How are weights initialized?
![WhatsApp Image 2021-09-24 at 10 01 11 PM](https://user-images.githubusercontent.com/75114179/134710119-40a9659a-2ee5-4d0c-9a74-d3cc20524cd6.jpeg)

*Title: Bell curve/Normal distribution curve with mean = 0, and -1 and +1 as end points*

The weights are randomly initialized, the distribution of which follows a normal curve, where mean tends to 0 and standard deviation varies between +1 or -1.

### 4. What is "loss" in a neural network?
![image](https://user-images.githubusercontent.com/75114179/134699434-4b354b21-9cbd-450b-89f6-30c56d8ba8e0.png)

   *LOSS:* Technically in simple words, ‘Loss’ helps us to understand how much the predicted value differ from actual value. Function used to calculate the loss is called as “Loss function”. At the end of each epoch the model calculates the loss, and inturn the weights are updated. The general aim of the model (for which purpose loss function is used)  is to minimize the loss.
   
 **Example:**
 
 ![image](https://user-images.githubusercontent.com/75114179/134700842-53f23120-837b-424c-b95d-e4fb0ba31226.png)
In the above example image of a simple NN with two outputs (cat and Dog), say cat is labelled as 0 and the dog is labelled as 1. As next step we pass an image of a cat to the model and the model outputs 0.25 for this image, then the error (loss) of the model would be predicted value 0.25 minus the actual data label 0 which is equal to 0.25 [This is the most simple L1 error or absolute error]. This is done for every input and at the end all the losses are added which is in turn passed through loss function.
   
   *LOSS FUNCTION:* Loss function is a method of evaluating “how well our algorithm models your dataset”. If our predictions are totally off, our loss function will output a higher number. If our predictions are good, i.e., closer to the desired output, it’ll output a lower number. As we tune our algorithm to try and improve the model, your loss function will tell us if we are improving or not. 
   
### 5. What is the "chain rule" in gradient flow?



