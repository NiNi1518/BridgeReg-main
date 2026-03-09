# BridgeReg

## Overview

This repository provides the official implementation of **BridgeReg**, a framework designed for multimodal cardiac MRI registration.

The proposed method aims to address the challenges of multimodal alignment and pathological region identification in cardiac MR images.

## Dataset Structe
```
|-train
    |- Casexx
        |-Casexx_C0_xx.nii.gz
        |-Casexx_LGE_xx.nii.gz
        |-Casexx_T2_xx.nii.gz
        |-Casexx_C0_gd_xx.nii.gz
        |-Casexx_LGE_gd_xx.nii.gz
        |-Casexx_T2_gd_xx.nii.gz
    |- ...
|-test
    |- Casexx
        |-Casexx_C0_xx.nii.gz
        |-Casexx_LGE_xx.nii.gz
        |-Casexx_T2_xx.nii.gz
        |-Casexx_C0_gd_xx.nii.gz
        |-Casexx_LGE_gd_xx.nii.gz
        |-Casexx_T2_gd_xx.nii.gz
    |- ...
```

## Implementation details
To train the model, run this command:
```
python registration-main.py --experiment 'your_expname' --phase 'train'
```
To evaluate pretrained model, run:
```
python registration-main.py --experiment 'your_expname' --phase 'test' --ckpt -1
```
