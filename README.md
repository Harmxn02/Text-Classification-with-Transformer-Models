# Text Classification with Pre-Trained Transformer Models

## Comparison of pre-trained models (and fine-tune [FT])

Here you will find the comparisons of all the different pre-trained models we tested, and trained.

The models were trained locally using an NVIDIA RTX 3060 Laptop GPU (6GB VRAM), and 32GB of RAM.

> We always train 3 epochs, with a batch size of 16, and a learning rate of 1e-5. Some models I trained multiple times, so you will find the same models in the table more than once.

| Model codename                       | Training time (m) | Test Accuracy | Test Loss Test | F1 Score |
| ------------------------------------ | ----------------- | ------------- | -------------- | -------- |
| `distilbert/distilbert-base-uncased` | 3m30s             | 0.889         | 0.346          | 0.889    |
| `distilbert/distilbert-base-uncased` | 3m24              | 0.897         | 0.352          | 0.897    |
| `xlnet/xlnet-base-cased`             | 8m39              | 0.872         | 0.390          | 0.871    |
| `google-bert/bert-base-uncased`      | 6m38              | 0.883         | 0.371          | 0.883    |
