# From sparse representations to Language Models

## Sparse representations

In the retrieval context, we've already introduced sparse text representations ([BOW, TF-IDF](sparse-bow-tfidf.md), [BM25](sparse-bm25.md)): they are simple and fast to use. On the other hand, they don't capture semantic similarity and don't take word order into account.

To understand the rise of more expressive textual representations, we need to step back and focus on word representations. Then we can transfer the same reasoning to document representations.

When using sparse representations, no proximity relationship emerges when examining the vectors corresponding to the words "dog" 🐕, "cat" 🐈, and "printer" 🖨️.

## Word embeddings

Starting from the 80s, word embeddings appeared. They are based on the distributional hypothesis (a word is characterized by the company it keeps).

A very popular example is Word2vec: it is a shallow neural network that is trained on a large linguistic corpus to predict a term given the surrounding words.
Once trained, the model produces a vector space (of several hundred dimensions), where each word has a corresponding vector.

If we look at the vector space, semantic relationships emerge.

One of the major shortcomings of these models is that each word corresponds to a single vector, even though that term can have different meanings in different contexts.

## Language models

The last few years have seen the introduction of Language Models (BERT, GPT), which have quickly dominated the world of Natural Language Processing!

They are neural networks that implement the Transformer architecture. They are trained on massive linguistic corpora, to predict some masked words given the context.
Once trained, they incorporate rich textual knowledge.

The key element of Transformers is the **attention mechanism**. When it comes to textual representation, we can intuitively say that for each word, the corresponding vector also takes into account the terms that make up the context. The embedding can be considered a weighted average.

In addition to achieving the state of the art in countless NLP tasks, these models open the door to dense retrieval...

Stay tuned 📻!

## Resources
- [What Is Text Vectorization? Everything You Need to Know: A guide to the history and the role of text vectorization in semantic search systems](https://www.deepset.ai/blog/what-is-text-vectorization-in-nlp): Deepset's blogpost explaining the entire journey from Bag-of-words to Dense Retrieval