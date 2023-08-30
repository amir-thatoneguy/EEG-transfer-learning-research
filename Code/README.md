This little jupyter notebook contains many experiments I did for this project. Most of the results are on the BCICIV-2a (BCI Competition IV) dataset. The datasets contains EEG recordings from 9 subjects. The goal is to correctly predict the intended movement from the EEG samples (left/right arm, left/right leg). I simplified the problem to a binary classification (left/right hand) and tried to predict the intended movement of a subject using a model trained on the labeled data of other subjects + unlabeled data of the current subject. The mean accuracy for each subject is then reported. 

The experiments I did include: 
- Variations the classic Euclidean Alignment (2018) approach to EEG transfer learning and adding EA to deep models (EEGNet and later the EEG Conformer (2023).
- Mixing up the covariance matrices of different subjects
- Kernel alignment
- Feature augmentation
- VAEs
- Visualizations for experiments

