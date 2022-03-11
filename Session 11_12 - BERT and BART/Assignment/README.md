### Assignment

These are the assignments that you'd be doing this and next week!

* TASK 1 (Week 1): Train BERT using the code mentioned here (https://drive.google.com/file/d/1Zp2_Uka8oGDYsSe5ELk-xz6wIX8OIkB7/view) on the Squad Dataset for 20% overall samples (1/5 Epochs). Show results on 5 samples. 
* TASK 2 (Week 1): Reproductive these (https://mccormickml.com/2019/07/22/BERT-fine-tuning/) results, and show output on 5 samples.
* TASK 3 (Week 2): Reproduce the training explained in this blog (https://towardsdatascience.com/bart-for-paraphrasing-with-simple-transformers-7c9ea3dfdd8c). You can decide to pick fewer datasets. 

Proceed to Session 11 - Assignment Solutions page and:
* Submit README link for Task 1 (training log snippets and 5 sample results along with BERT description must be available) - 750
* Submit README link for Task 2 (training log snippets and 5 sample results) - 250
* Submit README link for Task 3 (training log snippets and 5 sample results along with BART description must be available) - 1000

# TASK 1

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


# TASK 2

Reproduce these https://mccormickml.com/2019/07/22/BERT-fine-tuning/ results, and show output on 5 samples

## BERT Fine-Tuning Tutorial with PyTorch

The code shows how to use BERT with the huggingface PyTorch library to quickly and efficiently fine-tune a model to get near state of the art performance in sentence classification. 

### What is BERT?
BERT (Bidirectional Encoder Representations from Transformers), released in late 2018, is the model we will use in this tutorial to provide readers with a better understanding of and practical guidance for using transfer learning models in NLP. BERT is a method of pretraining language representations that was used to create models that NLP practicioners can then download and use for free. You can either use these models to extract high quality language features from your text data, or you can fine-tune these models on a specific task (classification, entity recognition, question answering, etc.) with your own data to produce state of the art predictions.

### Advantages of Fine-Tuning
* Quicker development
* Lesser data
* Better results

In the notebook, we make use of https://nyu-mll.github.io/CoLA/ dataset for single sentence classification. It’s a set of sentences labeled as grammatically correct or incorrect. It was first published in May of 2018, and is one of the tests included in the “GLUE Benchmark” on which models like BERT are competing
The dataset is hosted on GitHub in this repo: https://nyu-mll.github.io/CoLA/


### Parse
We can see from the file names (once unzipped) that both tokenized and raw versions of the data are available.
We can’t use the pre-tokenized version because, in order to apply the pre-trained BERT, we must use the tokenizer provided by the model. This is because:
(1) the model has a specific, fixed vocabulary and 
(2) the BERT tokenizer has a particular way of handling out-of-vocabulary words.

### BERT Tokenizer
To feed our text to BERT, it must be split into tokens, and then these tokens must be mapped to their index in the tokenizer vocabulary.
The tokenization must be performed by the tokenizer included with BERT

### Special Tokens
[SEP]
At the end of every sentence, we need to append the special [SEP] token.
This token is an artifact of two-sentence tasks, where BERT is given two separate sentences and asked to determine something (e.g., can the answer to the question in sentence A be found in sentence B?).

[CLS]
For classification tasks, we must prepend the special [CLS] token to the beginning of every sentence.
This token has special significance. BERT consists of 12 Transformer layers. Each transformer takes in a list of token embeddings, and produces the same number of embeddings on the output (but with the feature values changed, of course!).

![image](https://user-images.githubusercontent.com/75114179/157842673-02dc00d7-6288-4c89-9bce-215c3b2cd866.png)

### Sentence Length & Attention Mask
#### The sentences in our dataset obviously have varying lengths, so how does BERT handle this?

BERT has two constraints:

* All sentences must be padded or truncated to a single, fixed length.
* The maximum sentence length is 512 tokens.
* Padding is done with a special [PAD] token, which is at index 0 in the BERT vocabulary. The below illustration demonstrates padding out to a “MAX_LEN” of 8 tokens.
* 
![image](https://user-images.githubusercontent.com/75114179/157842864-de1f8d5b-bd3d-4c63-b3ae-dd33699152e8.png)

The “Attention Mask” is simply an array of 1s and 0s indicating which tokens are padding and which aren’t.

#### All of the model's parameters as a list of tuples
<img width="600" alt="image" src="https://user-images.githubusercontent.com/75114179/157843357-3cefbe84-32ef-48c5-b672-48020c45c950.png">

#### Training logs

<img width="500" alt="image" src="https://user-images.githubusercontent.com/75114179/157843546-aae4604a-0be5-4f7e-8001-eada8079b0e2.png">
<img width="500" alt="image" src="https://user-images.githubusercontent.com/75114179/157843648-68240193-9d8b-47d1-9880-2ca03cdef0fb.png">
<img width="500" alt="image" src="https://user-images.githubusercontent.com/75114179/157843684-8d6fadce-1456-4400-b844-f05af2c1915b.png">
<img width="500" alt="image" src="https://user-images.githubusercontent.com/75114179/157843712-64aa6205-89b2-4c92-826f-a869c4e1a4e0.png">

##### Consolidated 
<img width="600" alt="image" src="https://user-images.githubusercontent.com/75114179/157843777-1018bad4-0361-4abf-88ba-746a291bf997.png">

#### Training and Validation Loss
![image](https://user-images.githubusercontent.com/75114179/157843841-7164c9db-3eae-440c-80c4-4666eb9ea4e3.png)

# TASK 3
Reproduce the training explained in this blog (https://towardsdatascience.com/bart-for-paraphrasing-with-simple-transformers-7c9ea3dfdd8c). 

## BART for Paraphrasing with Simple Transformers
Paraphrasing is the act of expressing something using different words while retaining the original meaning, which in the notebook will be achieved with BART, a Sequence-to-Sequence Transformer Model. For the task of paraphrasing, the pre-trained BART model can be fine-tuned directly using the input sequence (original phrase) and the target sequence (paraphrased sentence) as a Sequence-to-Sequence model

### What is BART?
BART is a denoising autoencoder for pretraining sequence-to-sequence models. BART is trained by:
(1) corrupting text with an arbitrary noising function, and 
(2) learning a model to reconstruct the original text

#### BART Sequence-to-Sequence
BART has both an encoder (like BERT) and a decoder (like GPT), essentially getting the best of both worlds.
The encoder uses a denoising objective similar to BERT while the decoder attempts to reproduce the original sequence (autoencoder), token by token, using the previous (uncorrupted) tokens and the output from the encoder
![image](https://user-images.githubusercontent.com/75114179/157860906-6454b2d7-b3dd-4fb9-adcd-8b7c497cf5ab.png)

#### Some of the corruptionn schemes that can used for BART:
* Token Masking — A random subset of the input is replaced with [MASK] tokens, like in BERT.
* Token Deletion — Random tokens are deleted from the input. The model must decide which positions are missing (as the tokens are simply deleted and not replaced with anything else).
* Text Infilling — A number of text spans (length can vary) are each replaced with a single [MASK] token.
* Sentence Permutation — The input is split based on periods (.), and the sentences are shuffled.
* Document Rotation — A token is chosen at random, and the sequence is rotated so that it starts with the chosen token

