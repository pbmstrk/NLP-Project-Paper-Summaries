# Summary: Reading Wikipedia to Answer Open-Domain Questions

Chen et al. (2017) tackled open-domain question answering using Wikipedia as the sole knowledge source. 

They proposed a model, DrQA; combining approaches from document retrieval and machine reading.

DrQA consists of two modules,
1. Document Retriever, and
2. Document Reader

<p align="center">
  <img src="https://github.com/pbmstrk/NLP-Project-Paper-Summaries/blob/master/summaries/Reading%20Wikipedia%20to%20Answer%20Open-Domain%20Questions/fig/DrQA.png?raw=true" width=550px/>
  <br>
  <em>Overview of DrQA</em>
</p>

The purpose of the document retriever is to narrow the search space; that is, to retrieve the most relevant articles for answering the question. For this, the article and question are compared as TF-IDF weighted bag of words. Bigram features are also included to preserve information about local word ordering. In this way, the document retriever finds the five most relevant articles.

The document reader is a machine comprehension model that on a high level evaluates the similarity between the encoding of tokens in the paragraphs of an article and the question. Two separate classifiers are trained to predict the start and end of an answer span.