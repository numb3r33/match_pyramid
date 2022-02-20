# Match Pyramid
> Summary description here.


This file will become your README and also the index of your documentation.

## Install

`pip install matchpyramid`

## How to use

```python
#slow
dls, cnt = get_dls()
```

```python
#slow

glove            = get_glove_embeddings()
my_vocab         = get_my_vocab(cnt)
my_vocab.vectors = convert_cnt_to_glove_emb(my_vocab)

model = MatchPyramid(my_vocab, max_len=72)
learn = ImageTextLearner(dls, model, loss_func=BCEWithLogitsLossFlat())
```

```python
#slow
learn.lr_find()
```

```python
#slow
learn.fit_one_cycle(5, 1e-3)
```
