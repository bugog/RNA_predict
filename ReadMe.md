## RNA secondary structure prediction
This folder contains notbooks for rna secondary structure prediction.
All of them are based on the same method there are just few minor differences between the notbooks.

### How to run them?
All of them can be run separeatly from each other, however each contains functions to do the preprocessing setup, and those needs to be run only once per source folder. In the following I will tell how the base notebook "rna_2order_pred" (the others are variations of this one) can be run on your setup.

1. Firstly we need the following modules to be installed:
  imageio, scipy, numpy, tensorflow, pandas, PIL
2. Secondly in the end of the second cell one could preprocess the RNA files for later use. This is only needed to be done once for each folder. Note: if the notebooks works on the same data then only once in one notebook should be run the preprocess
3. Optional step: one could normalize the data so each class represented equaly uning the third cell. Similar to previous step only one run required.
4. In the 6th cell one could set hyperparamters such as, image resolution, batch size, learning rate, number of epochs
5. Also in the same cell the training data, evaluation data folders should be passed (using the preprocessed files) for the get_files() functions and, the logs_train_dir should be set to the log folder. The log folder will contain the saved models and it's data
6. In the last cell similarly to step 2 we need to preprocess testing data (once). The hyper paramets should remain the same except if the piture resolution was modified earlier, but batch size should be fixed as well as N_classes.
7. The model location should be set at the begining of the cell. It should be a saved checkpoint from one of the training earlier.

With these steps all the notebooks should be ready to run. As these are the same for all of them.

### Content:
The folder contains 5 variation for secondary sturcture prediction of RNAs and this ReadMe file.
1. "rna_2order_pred" - This is the base, 'vanila' edition which is the most basic implementation.
2. "l1regul" - This is a variation which uses L1 regularization
3. "l2regul" - This is a variation which uses L2 regularization
4. "dropout30" - This is a variation which 30% dropout rate in the dense layers
5. "4conv05drop" - This variation uses a more complex model with higher (50%) dropout rate.


```python

```
