<div align="center">

# CNN — CIFAR-10 Classification

**A convolutional network built in PyTorch to classify the 10 CIFAR-10 classes.**

*English* · [Português](#-português)

</div>

> 🇧🇷 **Português:** notebook em PyTorch que constrói uma CNN do zero (3 blocos convolucionais com BatchNorm, MaxPool, dropout) e a treina no CIFAR-10 para classificar as 10 classes de imagens.

## About

A complete, self-contained notebook covering the full deep learning workflow: data loading and augmentation, model definition, training loop, evaluation and visualisation. Written for Google Colab with optional GPU acceleration.

## Model architecture

```
Conv2d(3 → 16, k3, p1) + BatchNorm + ReLU + MaxPool
Conv2d(16 → 32, k3, p1) + BatchNorm + ReLU + MaxPool
Conv2d(32 → 64, k3, p1) + BatchNorm + ReLU + MaxPool
Flatten → Linear(64·4·4 → 128) + ReLU + Dropout(0.2)
Linear(128 → 10)
```

## Dataset

**CIFAR-10** — 60,000 32×32 colour images across 10 classes:

`plane`, `car`, `bird`, `cat`, `deer`, `dog`, `frog`, `horse`, `ship`, `truck`

Images are normalised with mean and standard deviation of `0.5` per channel; batches of 64 samples are used for training and evaluation.

## What the notebook covers

- Device selection (CUDA if available, otherwise CPU)
- Dataset download, normalisation and sample visualisation
- `DataLoader` setup with batch shape inspection
- CNN definition with `nn.Module`
- Training and evaluation on the test split

## How to run

```bash
git clone https://github.com/vitoriaayres/cnn.git
cd cnn
pip install torch torchvision matplotlib numpy
jupyter notebook CNN.ipynb
```

Or open it directly in **Google Colab** using the badge at the top of the notebook — PyTorch and CIFAR-10 download automatically.

## 🇧🇷 Português

- **O que é:** notebook de classificação de imagens com rede neural convolucional em PyTorch, treinada no CIFAR-10.
- **Arquitetura:** 3 blocos conv + BatchNorm + ReLU + MaxPool, camada densa de 128 unidades com dropout 0.2 e saída de 10 classes.
- **Dados:** CIFAR-10, 60 mil imagens 32×32, normalização com média/desvio 0.5, batch de 64.
- **Como rodar:** abra `CNN.ipynb` no Colab (badge no topo) ou localmente com `pip install torch torchvision matplotlib numpy`.

## Author

[Vitoria AYRES](https://github.com/vitoriaayres)
