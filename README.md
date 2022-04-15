# French T5 Abstractive Text Summarization

The files are available on [HuggingFace](https://huggingface.co/plguillou/t5-base-fr-sum-cnndm).

The easiest way to download and use it is to use Python (see below).

## Metrics

ROUGE-1: 44.5252

ROUGE-2: 22.652

ROUGE-L: 29.8866

## Model description

This model is a T5 Transformers model ([JDBN/t5-base-fr-qg-fquad](https://huggingface.co/JDBN/t5-base-fr-qg-fquad)) that was fine-tuned in french for abstractive text summarization.

## How to use

```python
from transformers import T5Tokenizer, T5ForConditionalGeneration
tokenizer = T5Tokenizer.from_pretrained("plguillou/t5-base-fr-sum-cnndm")
model = T5ForConditionalGeneration.from_pretrained("plguillou/t5-base-fr-sum-cnndm")
```

To summarize an ARTICLE, just modify the string like this : "summarize: ARTICLE".

## Training data

The base model I used is JDBN/t5-base-fr-qg-fquad (it can perform question generation, question answering and answer extraction).

I used the "t5-base" model from the transformers library to translate in french the CNN / Daily Mail summarization dataset.
