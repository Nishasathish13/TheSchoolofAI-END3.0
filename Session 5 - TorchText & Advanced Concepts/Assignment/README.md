Look at the code  (Links to an external site.)that we covered in the class today.

Pick any 2 datasets (except AG_NEWS) from torchtext.datasets and train your model on them achieving 50% more accuracy than random prediction. 
Upload to Github with a proper readme file describing your datasets, and showing your logs as well.

Have uploaded 3 ipynb notebooks for 3 datasets

## Dataset 1 : YelpReviewPolarity

https://pytorch.org/text/stable/_modules/torchtext/datasets/yelpreviewpolarity.html#YelpReviewPolarity
https://github.com/Nishasathish13/TheSchoolofAI-END3.0/blob/main/Session%205%20-%20TorchText%20%26%20Advanced%20Concepts/Assignment/Session_5_Assignment_dataset1.ipynb

<img width="550" alt="image" src="https://user-images.githubusercontent.com/75114179/151747595-ae34badf-33d4-4c1e-9ee1-7abb22068d22.png">

Labels: Numerical = 1 and 2

Training logs:

<img width="400" alt="image" src="https://user-images.githubusercontent.com/75114179/151747731-5593a5d9-6139-41af-8594-0d2de7c9bdde.png">
<img width="400" alt="image" src="https://user-images.githubusercontent.com/75114179/151747746-5fbe4076-8f5d-4ae6-91c4-5a429852e23c.png">

## Dataset 2 : IMDB

https://pytorch.org/text/stable/_modules/torchtext/datasets/imdb.html#IMDB
https://github.com/Nishasathish13/TheSchoolofAI-END3.0/blob/main/Session%205%20-%20TorchText%20%26%20Advanced%20Concepts/Assignment/Session_5_Assignment_dataset2.ipynb

<img width="550" alt="image" src="https://user-images.githubusercontent.com/75114179/151747955-2607c820-0619-4635-bad9-53a3c7573b5b.png">

Labels: String = 'pos' and 'neg'

Code to convert the string labels into numerical labels:

<img width="500" alt="image" src="https://user-images.githubusercontent.com/75114179/151748302-99f95125-d91a-40fd-bd6e-05e4e7da3aca.png">

Training logs:

<img width="400" alt="image" src="https://user-images.githubusercontent.com/75114179/151748351-660c3b10-8cac-45e8-90f2-ba619fa39f98.png">
<img width="400" alt="image" src="https://user-images.githubusercontent.com/75114179/151748365-952a1d50-8d01-48ea-94ee-0dd54731dcc6.png">



