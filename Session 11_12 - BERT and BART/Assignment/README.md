### Assignment

These are the assignments that you'd be doing this and next week!

* TASK 1 (Week 1): Train BERT using the code mentioned here (https://drive.google.com/file/d/1Zp2_Uka8oGDYsSe5ELk-xz6wIX8OIkB7/view) on the Squad Dataset for 20% overall samples (1/5 Epochs). Show results on 5 samples. 
* TASK 2 (Week 1): Reproductive these (https://mccormickml.com/2019/07/22/BERT-fine-tuning/) results, and show output on 5 samples.
* TASK 3 (Week 2): Reproduce the training explained in this blog (https://towardsdatascience.com/bart-for-paraphrasing-with-simple-transformers-7c9ea3dfdd8c). You can decide to pick fewer datasets. 

Proceed to Session 11 - Assignment Solutions page and:
* Submit README link for Task 1 (training log snippets and 5 sample results along with BERT description must be available) - 750
* Submit README link for Task 2 (training log snippets and 5 sample results) - 250
* Submit README link for Task 3 (training log snippets and 5 sample results along with BART description must be available) - 1000

#### TASK 1

Train BERT using the code mentioned here (Links to an external site.) on the Squad Dataset for 20% overall samples (1/5 Epochs). Show results on 5 samples. 

#### Squad dataset: https://rajpurkar.github.io/SQuAD-explorer/
The Stanford Question Answering Dataset (SQuAD) is a prime example of large-scale labeled datasets for reading comprehension. Rajpurkar et al. developed SQuAD 2.0, which combines 100,000 answerable questions with 50,000 unanswerable questions about the same paragraph from a set of Wikipedia articles. The unanswerable questions were written adversarially by crowd workers to look similar to answerable ones.

#### BERT
BERT is a trained Transformer Encoder stack, with twelve in the Base version, and twenty-four in the Large version. BERT was trained on Wikipedia and Book Corpus, a dataset containing +10,000 books of different genres.


* doc_tokens describes the context, i.e. the text which we want our model to understand.
* question_text describes the question which should be answered from the context.
* orig_answer_text represents the correct answer to the question.
* The answer is always a portion from the context starting at start_position and ending at end_position. 
* If the question does not have any answer in the context, is_impossible has the value true.
<img width="700" alt="image" src="https://user-images.githubusercontent.com/75114179/152332535-f6a90441-c1a3-483a-90f2-3808e7b70146.png">

<img width="700" alt="image" src="https://user-images.githubusercontent.com/75114179/152332779-9856fc3c-8722-47d5-bdfe-62052e26fca7.png">

#### Training logs

<img width="696" alt="image" src="https://user-images.githubusercontent.com/75114179/152490717-47e4a9f0-0a9e-4743-8805-86eba0a9e4fa.png">





