# Summary: Negated LAMA - Birds cannot fly?

Building on previous work examining how much relational knowledge is stored in pre-trained language models (Petroni et al., 2019) Kassner and Schütze (2019) investigated the ability of these models to understand and recall factual knowledge in negated statements. For this, negation was added to the cloze style questions in the LAMA dataset (e.g. "The theory of relativity was not developed by [MASK].").

The models were queried using both the original and negated statements; predictions for both queries largely overlapped. This suggests that negation is not understood and the models rely on the co-occurrence of the subject and relation in the training data, and thus simply memorise a few aspects of the facts. Another drawback is that the querying and evaluation setup does not allow the model to refrain from answering. 



