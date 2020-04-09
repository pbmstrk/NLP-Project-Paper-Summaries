# Summary: Language Models as Knowledge Bases?

Petroni et al. (2019) investigated how much relational knowledge is stored in the parameters of pre-trained language models. For this, they introduced the LAMA (LAnguage Model Analysis) probe; a collection of facts (which are either subject-relation-object triples or question-answer pairs) compiled from various knowledge sources.

The main of the idea of the LAMA probe is to express facts as cloze style questions and assess whether the model can accurately predict the masked tokens. The model was evaluated using a rank-based metric; measuring how highly the prediction of the ground truth token ranks among predictions for all other tokens in the vocabulary.

<p align="center">
  <img src="https://github.com/pbmstrk/NLP-Project-Paper-Summaries/blob/master/summaries/Language%20Models%20as%20Knowledge%20Bases%3F/fig/QueryingLanguageModels.png?raw=true" alt="Querying LMs and KBs for factual knowledge"/>
  <em>Querying LMs and KBs for factual knowledge</em>
</p>

