# Hottel Zone Physics-Constrained Networks (HZPCNet)


```
(Official) Github repository for our paper Hottel Zone Physics-Constrained Networks for Furnaces: From MLP and LSTM to KAN
```


## NOTE
This repository serves as a centralized hub for all resources related to the mentioned paper, including data, code, checkpoints, contact information, and additional webpages. Any future updates or modifications to these resources will be documented here. Interested users can visit this repository as a single starting point for easy access to the necessary pointers for their work.

## PACKAGE DEPENDENCIES

Package Requirements:
```
pandas, numpy, pytorch, seaborn, matplotlib, sklearn
```


## 1. PROCESSED DATA:

### 1.1 CONFIGURATION DATASET FILES

Create a directory called ```<parent_directory>/input_data/data_L_1/configs_csv/``` for storing the configuration/dataset files, which can be downloaded from the following link:
https://drive.google.com/drive/folders/11yvnHoBA5n8AIvSM_Lg8b3gTPMuBQAMQ?usp=sharing

The above directory contains 50 files, which occupy a combined disk space of ```1.35 GB```. Each file represents a configuration dataset, representing data belonging to a particular configuration of the furnace. As each of the configuration datasets are distinct, there is no overlap among a pair of files. Some of them are used collectively for training a model, and then the model is evaluated on a set of datasets for testing the model performance.

```<parent_directory>``` is the root project directory ```HZPCNet```, and is stored as the variable ```repo_path_prefix``` in the training scripts.

### 1.2 CONSOLIDATED CONFIGURATION DATASET SPLITS

To save time, a ```.npz file``` containing pre-processed data can be stored in the following location:
```<parent_directory>/input_data/data_L_1/pre_saved_npfiles/zonenet_npfile.npz```

This file can be downloaded from the following link:
https://drive.google.com/file/d/1ZaVGTVlbDl0hoo0Cm9zICkAPPqlaaUMV/view?usp=sharing 

## 2. TOTAL EXCHANGE AREA FILES

The TEA files are present in:
```<parent_directory>/input_data/<TEA>.txt```

where, ```<TEA>: {GG, SS, SG, GS}```

Link to GG file:
https://drive.google.com/file/d/1TiXX42AXCeQfss1YhwCA7htJEChaxb5e/view?usp=sharing

Link to GS file:
https://drive.google.com/file/d/1FQrGMc6-Ubm6oD7BNICzLH_zPTSvUAJa/view?usp=sharing

Link to SG file:
https://drive.google.com/file/d/1xCDhNNKi1O01dMjYA6aC4ApPiMHq9GC_/view?usp=sharing

Link to SS file:
https://drive.google.com/file/d/152YiBLg7v8NyWhSueWZ9rzJLD9j6ai2Q/view?usp=sharing


## 3. MODEL TRAINING SCRIPT DEMO

Path to directory containing model training scripts for a model ```<model_name>```:
```<parent_directory>/scripts_train/data_L/v2_scripts/<model_name>```

where we can have ```<model_name> : {PBDLSTM, PBKAN, … }``` for different methods. Here, we present a sample jupyter notebook for ```PBDLSTM```.

The network architectures for other methods are inspired from the following links:

3.1 KAN: https://github.com/KindXiaoming/pykan 

3.2 xLSTM: https://github.com/NX-AI/xlstm 
