Train the same code, but on different data. If you have n-classes, your accuracy MUST be more than 4 * 100 / n.

Submit the Github link, that includes your notebook with training logs, and proper readme file.

Dataset used: https://www.kaggle.com/kaushal2896/english-to-german

Snippets of code for data preprocessing used from: https://www.kaggle.com/kaushal2896/machine-translation-using-attention-rnn-gru

Code references: https://github.com/bentrevett/pytorch-seq2seq

## Data
<img width="700" alt="image" src="https://user-images.githubusercontent.com/75114179/151688573-aedfc035-32b3-4886-8c8c-fb5238323c55.png">

Choosing the 1st and 2nd column of the data:

<img width="599" alt="image" src="https://user-images.githubusercontent.com/75114179/151688589-7eee4342-5b29-4cf5-a6f3-e99044429f64.png">

<img width="200" alt="image" src="https://user-images.githubusercontent.com/75114179/151688625-90fe5a96-c5a9-4c3b-bd97-8842c7d027cc.png">

Plotting distribution of the sentences according to their lengths:

![image](https://user-images.githubusercontent.com/75114179/151688669-fd1e645b-c8d0-4b7e-8e6d-dc79bfd93cd6.png)

Training data and Validation data:

<img width="600" alt="image" src="https://user-images.githubusercontent.com/75114179/151688782-7a7bc736-3c9b-4e0d-be35-20f4a5d6fee5.png">

Due to computation compatibility subset of the above data will be used for Training purpose.

Sample data:

<img width="600" alt="image" src="https://user-images.githubusercontent.com/75114179/151688824-1cbd6341-acf7-43e4-80d2-9285daffb505.png">

Train logs:

<img width="600" alt="image" src="https://user-images.githubusercontent.com/75114179/155757592-2d98745c-f8b7-4c02-808b-dea368e9ab20.png">

