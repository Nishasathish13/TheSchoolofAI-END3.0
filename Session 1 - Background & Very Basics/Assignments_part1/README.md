# ASSIGNMENT PART 1
## Assignment Part 1 consists of an .ipynb notebook along with required description


# ASSIGNMENT PART 2
## Assignment part 2 is a descriptive section describing the below concepts.

### 1. What is a neural network neuron?
### 2. What is the use of the learning rate?
### 3. How are weights initialized?
### 4. What is "loss" in a neural network?
![image](https://user-images.githubusercontent.com/75114179/134699434-4b354b21-9cbd-450b-89f6-30c56d8ba8e0.png)

   *LOSS:* Technically in simple words, ‘Loss’ helps us to understand how much the predicted value differ from actual value. Function used to calculate the loss is called as “Loss function”. At the end of each epoch the model calculates the loss, and inturn the weights are updated. The general aim of the model (for which purpose loss function is used)  is to minimize the loss.
   
 **Example:**
 
 ![image](https://user-images.githubusercontent.com/75114179/134700842-53f23120-837b-424c-b95d-e4fb0ba31226.png)
In the above example image of a simple NN with two outputs (cat and Dog), say cat is labelled as 0 and the dog is labelled as 1. As next step we pass an image of a cat to the model and the model outputs 0.25 for this image, then the error (loss) of the model would be predicted value 0.25 minus the actual data label 0 which is equal to 0.25. This is done for every input and at the end all the losses are added which is in turn passed through loss function.
   
   *LOSS FUNCTION:* Loss function is a method of evaluating “how well our algorithm models your dataset”. If our predictions are totally off, our loss function will output a higher number. If our predictions are good, i.e., closer to the desired output, it’ll output a lower number. As we tune our algorithm to try and improve the model, your loss function will tell us if we are improving or not. 
### 5. What is the "chain rule" in gradient flow?


