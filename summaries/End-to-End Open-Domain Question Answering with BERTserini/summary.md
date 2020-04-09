# Summary: End-to-End Open-Domain Question Answering with BERTserini

Yang et al. (2019) address the open-domain question using a retrieve-then-read approach. For retrieval the IR (Information Retrieval) toolkit Anserini is used, and BERT is used for the machine reading component.

<p align="center">
  <img src="https://github.com/pbmstrk/NLP-Project-Paper-Summaries/blob/master/summaries/End-to-End%20Open-Domain%20Question%20Answering%20with%20BERTserini/fig/BERTserini.png?raw=true"/>
  <br>
  <em>Architecture of BERTserini</em>
</p>

For retrieval, a single-stage retriever is used that directly identifies relevant sections of text from Wikipedia (as opposed to a system that selects and ranks passages). The retrieved segments of text are then passed to the BERT reader. 

The BERT reader used is the same as originally proposed by [Devlin et al. (2018)](https://arxiv.org/abs/1810.04805).

At inference time, the Anserini retrieval component retrieves relevant sections and the BERT reader processes each section in turn. For each section, BERT predicts the start and end of the answer span and score rating the predicted span. The final score of the answer span is calculated as a linear combination of the score returned by the Anserini retriever and the BERT reader. 




