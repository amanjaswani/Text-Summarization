# Text-Summarization
Text summarization is the process of selecting important information from a piece of text in
such a way that the generated summary is in coherence with the actual text. The principal objective
is to get a subset of the actual text, which conveys all the important information of the whole text. It
is also important to ensure that the fluency of the generated summary is in accordance with the
language constructs.

We found that there are three common approaches:
1. Extractive text summarization (Textrank)
2. Abstractive text summarization (using LSTM with Attention mechanism)
3. Pointer Generator

The extractive text summarization technique involves pulling keyphrases from the source
document and combining them to make a summary. The extraction is made according to the defined
metric without making any changes to the text. This is implemented using TextRank Algo.
BERT word embeddings also used for the same (run BERT file on kaggle kernel only).

The abstractive text summarization technique on the other hand first understands the entire
task and then tries to build summary which may or may not contains words which were present in
original text. This approach is closer to human generated summaries but also, more difficult to
implement at the same time. Bidirectional LSTM with attention mechanism was used for this approach.

Data Link - https://www.kaggle.com/snap/amazon-fine-food-reviews

Ensemble model, called pointer-generator. 
This approach decides when to generate a word (abstractive) and
when to copy a word (extractive) with the help of a probability variable - p_gen. Whenever
the model encounters an out of vocabulary word or a word whose probability of prediction is
very less (prediction probability being decided by the attention mechanism from approach 6),
the model decides to behave extractively and copies words/phrases from the original text.

Data Link for Pointer Generator model - https://drive.google.com/open?id=1m4JltvmtoW8diZUfnxump_1u2ja7Du5R
Original Data - https://www.kaggle.com/sunnysai12345/news-summary
Preprocessing performed as explained by - https://github.com/becxer/cnn-dailymail/
