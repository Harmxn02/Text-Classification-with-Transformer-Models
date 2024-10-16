# Text Classification with Pre-Trained Transformer Models

## Comparison of pre-trained models (and fine-tune [FT])

Here you will find the comparisons of all the different pre-trained models we tested, and trained.

The models were trained locally using an NVIDIA RTX 3060 Laptop GPU (6GB VRAM), and 32GB of RAM.

| Model codename               | Model in code                         | Training time (m) | (FT) Learning Rate | (FT) Epochs | (FT) Batch size | Test Accuracy | Test Loss Test | F1 Score |
| ---------------------------- | ------------------------------------- | ----------------- | ------------------ | ----------- | --------------- | ------------- | -------------- | -------- |
| 1. `distilbert-base-uncased` | `DistilBertForSequenceClassification` | 3m30s             | 1e-5               | 3           | 16              | 0.916         | 0.275          | 0.917    |




<!-- I have only done 1 model so far -->

<!-- | `bert-base-uncased`       | `BertForSequenceClassification`       | 6m33s             | 1e-5               | 3           | 16              | 0.901         | 0.344          | 0.901    |
| `roberta-base`            | `RobertaForSequenceClassification`    | 6m47s             | 1e-5               | 3           | 16              | 0.850         | 0.451          | 0.850    |
| `xlnet-base-cased`        | `XLNetForSequenceClassification`      | 9m05s             | 1e-5               | 3           | 16              | 0.856         | 0.420          | 0.856    |
| `FINETUNED`               | `---`                                 | 8m09s             | 1e-5               | 5           | 32              | 0.823         | 0.609          | 0.823    | -->
