# Sparse retrieval: BM25

We have already introduced the simplest sparse representations for retrieval: [Bag-of-words and TF-IDF](sparse-bow-tfidf.md).

Let's recall the idea of TF-IDF:

Build a vocabulary composed of all the words in your collection of documents.
For each document, construct a vector with the same length as the vocabulary.
- Put a 0 for each missing word.
- If the word is present, put a weight that is greater the more the word is repeated in the document and is less the more the term is repeated within the corpus

**BM25** was developed in the 70s and 80s as an evolution of the TF-IDF.
This algorithm represents the de facto standard for sparse retrieval.
It is commonly and effectively used in real-world search engines. One of its most common implementations is found in Apache Lucene, the engine 🚂 that powers Elasticsearch, OpenSearch and Apache Solr!


 ![BM25 Formula](../images/bm25_equation.png) 

The formula may sound scary but in practice, it focuses on two aspects that were ignored by TF-IDF: term saturation and document length normalization.

## Term Saturation
Is a word that appears in the document 100 times much more relevant than another word that appears 20 times?

We can reasonably assume that if a term occurs more times than a certain saturation threshold, it does not make the document more relevant to that term.

In BM25, the term saturation is determined by the parameter `k1`.

## Document length normalization

A certain document contains the word "cake" once and is one page long. Another document contains the same word once but is 100 pages long.
Which document is more relevant to the query "cake"? 🍰

BM25 takes document length into account, penalizing longer documents through the parameter `b`.

## Resources
- [Understanding Term-Based Retrieval Methods in Information Retrieval](https://towardsdatascience.com/understanding-term-based-retrieval-methods-in-information-retrieval-2be5eb3dde9f): great blogpost by Lan Chu which intuitively explains BM25
- [Practical BM25 - Part 2: The BM25 Algorithm and its Variables](https://www.elastic.co/blog/practical-bm25-part-2-the-bm25-algorithm-and-its-variables): Elastic post that elaborates on the BM25 formula
- [Which BM25 Do You Mean? A Large-Scale Reproducibility Study of Scoring Variants](https://link.springer.com/chapter/10.1007/978-3-030-45442-5_4): recent paper comparing most popular BM25 variants
- [Rank-BM25](https://github.com/dorianbrown/rank_bm25): simple python implementation of BM25 algorithms by Dorian Brown