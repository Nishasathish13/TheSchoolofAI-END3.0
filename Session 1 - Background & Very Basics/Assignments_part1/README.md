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

  Understanding the Chain rule with the help of an example and then generalizing it. 
 
 - Chain rule is a mathematical concept used in differential equation.

![WhatsApp Image 2021-09-25 at 7 55 29 AM](https://user-images.githubusercontent.com/75114179/134754808-76215052-7d26-4ac3-8610-302a873aacd6.jpeg)

Consider a multi layer neural network as in the above figure with four inputs namely, Age, Education, Income and Savings, and one output which predicts the probability of a person buying an insurance. In the hidden layer we have 2 neurons where the 1st neuron represents Awarenes and the 2nd neuron represents Affordability. Assuming Age and Education contributes to Awareness and Income and savings contributes to Affordability, the value of weights are denoted. The dotted line implies W (weights) = 0.

Presenting the above exact NN in generic way (most simplified) , in terms of mathematics just for the purpose of calculation.

![WhatsApp Image 2021-09-25 at 7 45 38 AM](https://user-images.githubusercontent.com/75114179/134754719-8deaca79-350c-42b9-b6ad-30f2ab9cee9e.jpeg)

In the above figure, Z is our output. To determine how much output changes for a given change in awareness (1st neuron of hidden layer), we have the equation as depicted in the below figure. Patial differential of Z w.r.t X.  Talking in terms of Insurance NN, how much the likelihood of a person buying the insurance changes w.r.t change in Awareness.

![WhatsApp Image 2021-09-25 at 7 46 15 AM](https://user-images.githubusercontent.com/75114179/134754723-14ecb1d8-47fb-4588-a180-4bdc2f87b36b.jpeg)

Next step we determine for a given change in **a** how much X changes, which is partial derivative of X w.r.t **a** . In context of Insurance NN, how much the Awareness changes w.r.t change in Age.

![WhatsApp Image 2021-09-25 at 7 47 19 AM](https://user-images.githubusercontent.com/75114179/134754727-ea77f82a-a0cc-4eeb-9400-7de4cb452ac8.jpeg)

Similarly we have change in Awareness w.r.t change in Education (represented by b)

![WhatsApp Image 2021-09-25 at 7 47 48 AM](https://user-images.githubusercontent.com/75114179/134754728-fc4ebe0e-76b5-4533-8ead-4540485be11a.jpeg)

Finally, the change in X w.r.t change in a or b is a chain rule where both the partial derivatives are multipllied as in the equation below.

![WhatsApp Image 2021-09-25 at 7 48 14 AM](https://user-images.githubusercontent.com/75114179/134754731-8464881d-e76b-4af3-ba2d-084fb02008f5.jpeg)

Extending the sam econcept ot the more generalized NN following the standard naming convention, Series of x as inputs, Activation function = tanh and weights as w1,w2..,wn also bias = False (only for easier computational purpose)

![WhatsApp Image 2021-09-25 at 7 48 32 AM](https://user-images.githubusercontent.com/75114179/134754737-4718e703-2a91-4e2a-8f1c-e8d43f53e80b.jpeg)

The final output is as below:

![WhatsApp Image 2021-09-25 at 7 49 00 AM](https://user-images.githubusercontent.com/75114179/134754739-527c881f-20a4-47f2-a0fa-b6a15ececb1e.jpeg)

Rewriting the partial derivatives with the new terminology, we get the below equations which is known as the chain rule. The derivatives give the slope of the tangent to the point which is basically the Gradient. 

![WhatsApp Image 2021-09-25 at 7 49 37 AM](https://user-images.githubusercontent.com/75114179/134754705-907cf415-e675-4a33-8566-dcf83e62f174.jpeg)






