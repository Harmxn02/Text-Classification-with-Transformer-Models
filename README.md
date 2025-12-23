# Text Classification with Pre-Trained Transformer Models

The models were trained locally using an NVIDIA RTX 3060 Laptop GPU (6GB VRAM), and 32GB of physical RAM.

EDIT: In the experimental section, I used an NVIDIA RTX 4070 Super (12GB VRAM), and 32GB of DDR5 RAM.

> We always train 3 epochs, with a batch size of 16, and a learning rate of 1e-5. Some models I trained multiple times, so you will find the same models in the table more than once.

| Model codename                       | Training time (m) | Test Accuracy | Test Loss | Test F1 Score |
| ------------------------------------ | ----------------- | ------------- | --------- | ------------- |
| `distilbert/distilbert-base-uncased` | 3m30s             | 0.889         | 0.346     | 0.889         |
| `distilbert/distilbert-base-uncased` | 3m24              | 0.897         | 0.352     | 0.897         |
| `xlnet/xlnet-base-cased`             | 8m39              | 0.872         | 0.390     | 0.871         |
| `google-bert/bert-base-uncased`      | 6m38              | 0.883         | 0.371     | 0.883         |

## Experimental

> in the `experimental.ipynb` notebook, we trained for 10 epochs, with a batch size of 32

EDIT: _Way later, I also trained it for 20 epochs on a stronger machine, same batch size of 32. For this run the classification report is all `1.00`_

| Model codename                         | Training time (m) | Test Accuracy | Test Loss | Test F1 Score |
| -------------------------------------- | ----------------- | ------------- | --------- | ------------- |
| `distilbert/distilbert-base-uncased`   | 10m38             | 0.970         | 0.107     | 0.970         |
| `distilbert/distilbert-base-uncased`\* | 6m38              | 0.999         | 0.009     | 0.999         |

### Classification report

|              | precision | recall | f1-score | support |
| ------------ | --------- | ------ | -------- | ------- |
| cajun_creole | 0.94      | 0.96   | 0.95     | 250     |
| chinese      | 0.98      | 1.00   | 0.99     | 250     |
| french       | 0.93      | 0.98   | 0.96     | 250     |
| indian       | 0.98      | 0.99   | 0.98     | 250     |
| italian      | 0.98      | 0.94   | 0.96     | 250     |
| mexican      | 0.99      | 0.97   | 0.98     | 250     |
| southern_us  | 0.96      | 0.95   | 0.96     | 250     |
| thai         | 1.00      | 0.97   | 0.98     | 250     |
|              |           |        |          |         |
| accuracy     |           |        | 0.97     | 2000    |
| macro avg    | 0.97      | 0.97   | 0.97     | 2000    |
| weighted avg | 0.97      | 0.97   | 0.97     | 2000    |

Pretty good, no?

Turns out training for a longer time improves your model's performance. Who could've guessed?

## Conclusion

The `distilbert/distilbert-base-uncased` model is the best model for this task. It has the best accuracy, loss, and F1 score. It is also the fastest to train, which is a huge plus.

## References

- [DistilBERT](https://huggingface.co/docs/transformers/model_doc/distilbert)
- [XLNet](https://huggingface.co/docs/transformers/model_doc/xlnet)
- [BERT](https://huggingface.co/docs/transformers/model_doc/bert)
