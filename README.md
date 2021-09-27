# model_card templates

We recommend sharing information about each model in a `model_card`.

The canonical documentation about model cards is at https://huggingface.co/docs/hub/model-repos and you can find a spec of the metadata at https://raw.githubusercontent.com/huggingface/huggingface_hub/main/modelcard.md.

One of the easiest way to get started is by using our template card. Simply copy `template.README.md` to `model_cards/USERNAME/MODELNAME/README.md` and fill it out while studying [demo.README.md](./demo.README.md) for an example of a model `model_card` and referring to rest of this short document if you are not sure about some specific fields.

## YAML metadata section

Here is a sample of a typical yaml metadata section:
```
---
language:
- ru
- en
thumbnail: https://raw.githubusercontent.com/JetRunner/BERT-of-Theseus/master/bert-of-theseus.png
tags:
- translation
- fsmt
license: apache-2.0
datasets:
- wmt19
metrics:
- bleu
- sacrebleu
---
```

**Important**:
* This section has to be first in the document, before any markdown sections.
* The data in this section doesn't need to be repeated again in the subsequent markdown sections - since it'll be automatically expanded into a user-friendly format on the website.

### language

ISO 639-1 code for your language (e.g. `ru`, `en`, `de`, or `multilingual`)

### thumbnail 

"url to a thumbnail used in social sharing"

### tags:
- array
- of
- tags

### license

One of the valid license identifiers. e.g.:

```
- apache-2.0
- mit 
```


### datasets

One or more dataset identifiers. 

Example:

```
- wmt19
- wmt16
```

You will find the supported list at https://huggingface.co/datasets

### metrics:

One or more metric identifiers. e.g.:

```
- bleu
- rouge
- sacrebleu
```

You will find the supported list at https://huggingface.co/metrics


## Markdown


# Model name

## Model description

You can embed local or remote images using `![](...)`

## Intended uses & limitations

#### How to use

```python
# You can include sample code which will be formatted
```

#### Limitations and bias

Provide examples of latent issues and potential remediations.

## Training data

Describe the data you used to train the model.
If you initialized it with pre-trained weights, add a link to the pre-trained model card or repository with description of the pre-training data.

## Training procedure

Preprocessing, hardware used, hyperparameters...

## Eval results

### BibTeX entry and citation info

```bibtex
@inproceedings{...,
  year={2020}
}
```
