# Summary: How Much Knowledge Can You Pack Into the Parameters of a Language Model?

The approach taken by Roberts et al. (2020) differs from previous work ([Petroni et al., 2019](https://www.aclweb.org/anthology/D19-1250/); [Jiang et al., 2019](https://arxiv.org/abs/1911.12543)) in two key ways. Firstly, earlier work evaluated the relational and factual knowledge in *off-the-shelf* language models, while Roberts et al. (2020) explicitly formulate the problem as an open-domain question answering task and fine-tune the model. Secondly, Roberts et al. (2020) treat the open-domain question answering problem as a text-to-text problem and make use of T5, a encoder-decoder Transformer. In this way, the model is trained to generate the text of the answer. This approach is *truly* open-domain, as no external information is used.

<p align="center">
  <img src="https://github.com/pbmstrk/NLP-Project-Paper-Summaries/blob/master/summaries/How%20Much%20Knowledge%20Can%20You%20Pack%20Into%20the%20Parameters%20of%20a%20Language%20Model%3F/fig/t5.png?raw=true" alt="Querying LMs and KBs for factual knowledge" width=650px/>
  <br>
  <em>T5 is fine-tuned to answer questions without any additional context</em>
</p>

