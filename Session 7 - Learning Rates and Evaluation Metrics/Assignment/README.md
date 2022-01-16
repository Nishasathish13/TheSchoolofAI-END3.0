# Assignment

Pick any of your past code and:

Implement the following metrics (either on separate models or same, your choice):
* Recall, Precision, and F1 Score
* BLEU 
* Perplexity (explain whether you are using bigram, trigram, or something else, what does your PPL score represent?)
* BERTScore

https://colab.research.google.com/drive/1kpL8Y_AnUUiCxFjhxSrxCsc6-sDMNb_Q

https://huggingface.co/metrics/bertscore

https://towardsdatascience.com/accuracy-precision-recall-or-f1-331fb37c5cb9

https://machinelearningmastery.com/calculate-bleu-score-for-text-python/

1. Explain Recall
<img width="430" alt="image" src="https://user-images.githubusercontent.com/75114179/149662328-86a721c6-6b77-4c91-abd2-2a3536ad5628.png">

<img width="248" alt="image" src="https://user-images.githubusercontent.com/75114179/149662149-0a40aa60-d161-49ea-8c0e-12ddcef2a63a.png">
Recall actually calculates how many of the Actual Positives our model capture through labeling it as Positive (True Positive). Recall shall be the model metric we use to select our best model when there is a high cost associated with False Negative.

2. Explain Precision
<img width="417" alt="image" src="https://user-images.githubusercontent.com/75114179/149662340-f067da7e-aaa0-4b25-86c5-93956fa4e7bf.png">
<img width="265" alt="image" src="https://user-images.githubusercontent.com/75114179/149662319-76b30428-b91f-4d0f-8c85-a8947de5bb3e.png">
Precision talks about how precise/accurate model is out of those predicted positive, how many of them are actual positive.
Precision is a good measure to determine, when the costs of False Positive is high. For instance, email spam detection. In email spam detection, a false positive means that an email that is non-spam (actual negative) has been identified as spam (predicted spam). The email user might lose important emails if the precision is not high for the spam detection model.

3. Explain F1 Score
<img width="188" alt="image" src="https://user-images.githubusercontent.com/75114179/149662423-d3d8bd6f-ecff-4343-82d6-0c359305db49.png">
F1 Score is the weighted average of Precision and Recall. Therefore, this score takes both false positives and false negatives into account. F1 is usually more useful than accuracy, especially if we have an uneven class distribution. Accuracy works best if false positives and false negatives have similar cost. If the cost of false positives and false negatives are very different, it’s better to look at both Precision and Recall

4. Explain BLEU score
<img width="188" alt="image" src="https://user-images.githubusercontent.com/75114179/149662682-7022c23b-476e-41df-81cf-56231bffa8dd.png">
BLEU, or the Bilingual Evaluation Understudy, is a score for comparing a candidate translation of text to one or more reference translation.A perfect match results in a score of 1.0, whereas a perfect mismatch results in a score of 0.0. "The primary programming task for a BLEU implementor is to compare n-grams of the candidate with the n-grams of the reference translation and count the number of matches. These matches are position-independent. The more the matches, the better the candidate translation is."

6. Explain Perplexity
In the BLEU score evalustion, because of huge corpus, the probabilistic numbers become so small that we will have floating point underflow. Hence the solution to the above problem is to define the probability of a sequence using Perplexity. It is defined as the exponential average negative log-likelihood of a sequence.
<img width="255" alt="image" src="https://user-images.githubusercontent.com/75114179/149664845-c54cd5b6-8063-4450-9b89-b511759a385c.png">
Perplexity can be thought as the reciprocal of probability, normalized by the sequence of length.

7. Explain BERT score
BERTScore leverages the pre-trained contextual embeddings from BERT and matches words in candidate and reference sentences by cosine similarity. It has been shown to correlate with human judgment on sentence-level and system-level evaluation. Moreover, BERTScore computes precision, recall, and F1 measure, which can be useful for evaluating different language generation tasks.

