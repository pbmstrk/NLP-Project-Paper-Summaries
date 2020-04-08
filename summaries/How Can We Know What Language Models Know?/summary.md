# Summary: How Can We Know What Language Models Know?

Jiang et al. (2019) set out to create a more accurate estimate of the knowledge contained in pre-trained language models. In previous work (Petroni et al., 2019),  only a single query was used, thus effectively providing a lower bound estimate on the information contained in the language models. By using multiples queries and combining answers from different queries \citeJiang et al. (2019) aimed to create a more accurate estimate.

To create queries, two approaches were used,
1. mining-based generation: using words that appear in the context of both the subject and object of a relation as prompts.
2. paraphrasing-based generation: paraphrase original prompt into semantically similar expressions.

To select prompts their accuracy in retrieving the ground truth was evaluated on a training set. 

When using combinations of different prompts the knowledge retrieval accuracy by $7\%$.