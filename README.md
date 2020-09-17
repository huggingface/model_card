# model_card templates

Here is how to create a model_card

Copy `template.README.md` to under `model_cards/USERNAME/MODELNAME/README.md` and fill it out while studying [demo.README.md](./demo.README.md) for an example of a model model_card and reading the rest of this document if you are not sure about some specific fields.

## YAML metadata section

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
- Apache 2.0
- MIT 
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
