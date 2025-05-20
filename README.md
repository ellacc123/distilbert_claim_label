# Claim Classification w/ Fine Tuning Models

## Hugging Face distilBert
info: https://huggingface.co/distilbert/distilbert-base-uncased

**1. Creating the Dataset**

0 = Invalid Claim

1 = Not a Scientific Claim

2 = Grey Area Claim 

3 = Scientific Claim

**2. Training the Model**
I first split the data into "training" and "testing" datasets, where 80% of the data will be used for training and 20% will be used for testing. 
I converted the data to PyTorch tensors which would be used to fine-tune Bert.

I set the model to train on the data for three epochs. 
I then trained it on the "train" (80%) portion of the data and evaluated it on the "test" (20%) of the data. 
This took about 5 minutes to run on my computer.

**3. Output: Confusion Matrix, Accuracy**
I outputted the confusion matrix as well as metrics (accuracy, precision, recall, F1-score) to depict the performance of the model.

Accuracy:  0.6613
Precision: 0.4508
Recall:    0.6613
F1 Score:  0.5353
