# pdb-secstr-pred

This repository contains a tensorflow model to predict protein secondary structure given the amino acid sequence. The model uses 3 bidirectional LSTM layers and is trained on the data available at https://cdn.rcsb.org/etl/kabschSander/ss.txt.gz

The model achieves an accuracy of 88% when predicting helix, sheet and others (3 labels). The model contained in this reposiory was trained on 80000 random samples and tested on 20000 samples.

The model details can be found in the file train.ipynb

To run the program from scratch, make sure you follow these steps:

1. Ensure you have prerequisite libraries installed (NumPy, pandas, Tensorflow)
2. Download the ss.txt file from the PDB website which can be found here.
3. Run all the blocks in the file format_code.ipynb to generate data.csv which contains formatted data from ss.txt.
4. Run all the bocks in the file train.ipynb to train and save the model. Note that hyperparameters like batch size and number of epochs can be changed accordingly.
5. Run the blocks in predict.ipynb to use the model to predict the structure for a given list of protein sequences.

For more information, comment on this repository or write to me at shrey16.sg@gmail.com
