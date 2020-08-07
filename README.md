# Paraphrase Detection on PAWS dataset
NLP models to identify paraphrases, on the paws dataset containing sentence pairs with high lexical overlap.

Below are two examples from the dataset:

|     | Sentence 1                    | Sentence 2                    | Label |
| :-- | :---------------------------- | :---------------------------- | :---- |
| (1) | Although interchangeable, the body pieces on the 2 cars are not similar. | Although similar, the body parts are not interchangeable  on the 2 cars.  | 0     |
| (2) | Katz was born in Sweden in 1947 and moved to New York City at the age of 1.      | Katz was born in 1947 in Sweden and moved to New York at the age of one.   | 1     |


https://github.com/google-research-datasets/paws
https://arxiv.org/abs/1904.01130


Used a bert base model with a classification layer on top available in the [Huggingface Transformers](https://huggingface.co/transformers/) library to classify the pairs. This model achieved an accuracy of 92%.

Analysed the errors this model was making using the pairs it classified wrongly (in 'wrongClassifications.tsv') and found out that the model had high confidence for wrongly classified data as well so there wasn't a margin below which we could assert uncertainty.

A report containing our findings are added [here](https://github.com/SaubanMusaddiq/Paraphrase_Detection_on_PAWS/blob/master/Phase1%20Report.pdf).
