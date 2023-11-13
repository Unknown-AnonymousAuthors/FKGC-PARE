# WWW2024-FKGC-PARE

## Steps to run the experiments

### Requirements

* ``Python 3.8.0 ``
* ``PyTorch 1.10.0``

### Datasets
We conduct our experiments on two datasets — NELL-One [here](https://github.com/xwhan/One-shot-Relational-Learning) and FB15k237-One [here](https://drive.google.com/drive/folders/16pamNJ-8gDPC2qaObN0pr93xeqdzq4Sq). 

Datasets used in this work [here](https://drive.google.com/drive/folders/1RZV8QC2D_0oexWRyj5yUL93YFNxz0ToI?usp=sharing).

### Pre-trained embeddings
* [NELL-One](https://drive.google.com/file/d/1XXvYpTSTyCnN-PBdUkWBXwXBI99Chbps/view?usp=sharing)
* FB15k237-One (We use this [repository](https://github.com/thunlp/OpenKE) to get the embeddings)

### Training

```python
cd code
python main.py --dataset "../data/NELL-One" --few n --max_batches 300000 --max_neighbor 50 --fine_tune
```

In this work, we set n=1 for one-shot and n=5 for five-shot. 

### Test
```python
python main.py --dataset "../data/NELL-One" --few n --test 1
```

