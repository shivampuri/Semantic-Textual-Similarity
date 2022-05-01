# Semantic-Textual-Similarity

#### Dipankar Saha &emsp;&emsp;&emsp;&emsp;&emsp; Shivam Puri &emsp;&emsp;&emsp;&emsp;&emsp;Vaibhav Gupta


## Abstract
Semantic Textual Similarity (STS) measures the meaning similarity of sentences. Applications of this task include machine translation, summarization, text generation, question answering, short answer grading, semantic search, dialogue and conversational systems. We developed Random Forest Regression model with various features. We have also trained sentence semantic representations with BiLSTM and BERT.

## Introduction
The goal of this task is to measure semantic textual similarity between a given pair of sentences (what they mean rather than whether they look similar syntactically). While making such an assessment is trivial for humans, constructing algorithms and computational models that mimic human level performance represents a difficult and deep natural language
understanding (NLU) problem.

#### Example 1:

English: Birdie is washing itself in the water basin.

English Paraphrase: The bird is bathing in the sink.

Similarity Score: 5 ( The two sentences are completely equivalent, as they mean the same thing.)

#### Example 2:

English: The young lady enjoys listening to the guitar.

English Paraphrase: The woman is playing the violin.

Similarity Score: 1 ( The two sentences are not equivalent, but are on the same topic. )

Semantic Textual Similarity (STS) measures the degree of equivalence in the underlying semantics of paired snippets of text. STS differs from both textual entailment and paraphrase detection in that it captures gradations of meaning overlap rather than making binary classifications of particular relationships. While semantic relatedness expresses a graded semantic relationship as well, it is non-specific about the nature of the relationship with contradictory material still being a candidate for a high score (e.g., “night” and “day” are highly related but not particularly similar). The task involves producing real-valued similarity scores for sentence pairs. Performance is measured by the Pearson correlation of machine scores with human judgments.

## Experimental Design

### Data
We obtained the data from year 2012 SemEval Shared Task. Out of a total of approximately 6000 sentence pairs, we were left with about 5750 sentence pairs (cleaning involved removing sentence pairs without a tab delimiter and pairs with a blank gold score). We split the data into three parts as below. 

- Training data: 4600 pairs
- Validation data:  575 pairs
- Test data: 575 pairs 

### Data Pre-processing

We used tokenization and lemmatization on the data as a pre-processing step before we turn the data into our models. We chose to do this step as lemmatization does not take away any semantic information from sentences and hence was an essential step for our application.

### Evaluation Metric
The official score is based on weighted Pearson correlation between predicted similarity and human annotated similarity. The higher the score, the better the the similarity prediction result from the algorithm.


## Files Submitted : 
- STS_TF-IDF_Word2Vec_BiLSTM.ipynb
- STS_BERT.ipynb
- STS_RoBERTa.ipynb
- STSData.csv
- Cleaned_STSData.csv
