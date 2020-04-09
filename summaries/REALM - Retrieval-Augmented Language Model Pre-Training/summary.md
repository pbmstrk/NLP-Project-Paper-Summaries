# Summary: REALM: Retrieval-Augmented Language Model Pre-Training

Motivated by earlier results illustrating the amount of factual and relational knowledge stored in pre-trained in language models ([Petroni et al., 2019](https://www.aclweb.org/anthology/D19-1250/)), Guu et al. (2020) propose a method to capture infornmation in a more interpretable manner. For this, they introduced a new framework for pre-training: Retrieval-Augmented Language Model. This approach augments the typical pre-training of language models with a knowledge retriever.

For both pre-training and fine-tuning REALM takes an input, <img src="https://render.githubusercontent.com/render/math?math=x"> and models a distribution <img src="https://render.githubusercontent.com/render/math?math=p(y | x)"> over the possible outputs <img src="https://render.githubusercontent.com/render/math?math=y">. In particular, REALM follows a *retrieve-then-predict* structure. In the retrieval step, possibly helpful documents <img src="https://render.githubusercontent.com/render/math?math=z"> are retrieved from a knowledge corpus. Then, to generate the output, condition on both the retrieved document and the original input, <img src="https://render.githubusercontent.com/render/math?math=p(y | x, z)">.

The architecture consists of two key components:
1. The knowledge retriever, which models <img src="https://render.githubusercontent.com/render/math?math=p(z | x)">, and
2. The knowledge-augmented encoder, which models <img src="https://render.githubusercontent.com/render/math?math=p(y | x, z)">.

<p align="center">
  <img src="https://github.com/pbmstrk/NLP-Project-Paper-Summaries/blob/master/summaries/REALM%20-%20Retrieval-Augmented%20Language%20Model%20Pre-Training/fig/REALM.png?raw=true"/>
  <br>
  <em>Overview of the REALM framework. Pre-training is shown on the left, and fine-tuning on the right</em>
</p>

The knowledge-retriever uses the inner product to compare the embeddings (computed using BERT) of the question and the document. A distribution over all documents in the corpus is then calculated.

For the knowledge-augmented encoder, the input and the retrieved document are combined into a single sequence. Then depending on whether pre-training or fine-tuning, either a masked language modeling loss is used, or the start and end of the answer span are predicted.

<p align="center">
  <img src="https://github.com/pbmstrk/NLP-Project-Paper-Summaries/blob/master/summaries/REALM%20-%20Retrieval-Augmented%20Language%20Model%20Pre-Training/fig/illustration.png?raw=true" height=300px/>
  <br>
  <em>Augmentation of language model pre-training</em>
</p>

To summarise, the knowledge-retriever finds the most similar passages to a question using BERT embeddings. The retrieved passaged is then added to the original input and a prediction is made.




