#### 1. Introduction

Achieve nueral machine translation from German to English by using Pytorch and Multi30K dataset with data augmentation.

#### 2.  Dependency requirements

PyTorch
TorchText

#### 3. File path settings and folder structure

The folder ''dataset-master'' is the Multi30K dataset we used in this project. The trained MT model and the translated texts of the test set will be saved in the same path as ```translation.py```.

#### 4. Running the code

Directly run the code ```python translation.py```.
The model willed be trained by using Multi30K and the trained model will be saved as ```model.pth```.
A loss curve of the training set and validation set will be shown.
The translated texts of the test set ```test_2016_flickr.de``` will be saved as ```tst.txt```.
You can use ```test_en.txt``` and ```multi-bleu.perl``` to get the blue score.

#### 5. Some functions explainations

```translate(model, src, src_vocab, tgt_vocab, src_tokenizer)```:
Translate a certain sentence by a model. It will return the translated sentence.

```parameter_performance()```:
Can choose and change hyperparameters and compare their performance via val_loss.

```train()```:
Train the ML model and plot a loss curve of the training set and validation. It will return the final val_loss.
