# Hottel Zone Physics-Constrained Networks (HZPCNet)


```
(Official) Github repository for our paper Hottel Zone Physics-Constrained Networks for Furnaces: From MLP and LSTM to KAN
```


## NOTE
This repository serves as a centralized hub for all resources related to the mentioned paper, including data, code, checkpoints, contact information, and additional webpages. Any future updates or modifications to these resources will be documented here. Interested users can visit this repository as a single starting point for easy access to the necessary pointers for their work.

For access to data, please refer https://github.com/ukdsvl/HZPCNet

Package Requirements:
pandas, numpy, pytorch, seaborn, matplotlib, sklearn, 

Path to directory containing model training scripts for a model <model_name>:
<parent_directory>/scripts_train/data_L/v2_scripts/<model_name>

where ,
<parent_directory> stored as variable repo_path_prefix in the training scripts.
<model_name> : {PBDLSTM, PBKAN, … }

Directory containing the configuration/dataset files:
<parent_directory>/input_data/data_L_1/configs_csv/

The above directory contains 50 files, which occupy a combined disk space of 1.35 GB. Each file represents a configuration dataset, representing data belonging to a particular configuration of the furnace. As each of the configuration datasets are distinct, there is no overlap among a pair of files. Some of them are used collectively for training a model, and then the model is evaluated on a set of datasets for testing the model performance.

To save time, a .npz file containing pre-processed data is provided in the following location:
<parent_directory>/input_data/data_L_1/pre_saved_npfiles/zonenet_npfile.npz

The TEA files are present in:
<parent_directory>/input_data/<TEA>.txt

where, <TEA>: {GG, SS, SG, GS} 

