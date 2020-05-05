# Paraphrase Detection on PAWS dataset
NLP models to identify paraphrases, on the paws dataset containing sentence pairs with high lexical overlap.

https://github.com/google-research-datasets/paws
https://arxiv.org/abs/1904.01130

## Phase 1:
For phase 1 we used a bert base model with a classification layer on top available in the [Huggingface Transformers](https://huggingface.co/transformers/) library to classify the pairs. This model achieved an accuracy of 92%.

We analysed the errors this model was making using the pairs it classified wrongly (in 'wrongClassifications.tsv') and found out that the model had high confidence for wrongly classified data as well so there wasn't a margin below which we could assert uncertainty.

A report containing our findings in phase 1 is added [here](https://github.com/SaubanMusaddiq/Paraphrase_Detection_on_PAWS/blob/master/Phase1%20Report.pdf).
