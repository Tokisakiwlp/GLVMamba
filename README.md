## Introduction
Official implementation for GLVMamba

## Datasets
  - [ISPRS Vaihingen and Potsdam](https://www.isprs.org/education/benchmarks/UrbanSemLab/default.aspx) 


## Folder Structure
```none
├── data
│   ├── vaihingen
│   │   ├── train_images (original)
│   │   ├── train_masks (original)
│   │   ├── test_images (original)
│   │   ├── test_masks (original)
│   │   ├── test_masks_eroded (original)
│   │   ├── train (processed)
│   │   ├── test (processed)
│   ├── potsdam (the same with vaihingen)
```

## Install
```
conda create -n RS python==3.8
conda install cudatoolkit==11.8 -c nvidia
pip install torch==1.10.0+cu111 torchvision==0.11.0+cu111 torchaudio==0.10.0 -f https://download.pytorch.org/whl/torch_stable.html
conda install -c "nvidia/label/cuda-11.8.0" cuda-nvcc
conda install packaging
cd CM-UNet
pip install -r requirements.txt
cd geoseg/Mamba-UNet
cd mamba
python setup.py install
cd ../ ; cd causal-conv1d
python setup.py install
```




## Acknowledgement

Many thanks the following projects's contributions to **GLVMamba**.
- [Mamba-UNet](https://github.com/ziyangwang007/Mamba-UNet)
- [GeoSeg](https://github.com/WangLibo1995/GeoSeg)
- [mmsegmentation](https://github.com/open-mmlab/mmsegmentation)


