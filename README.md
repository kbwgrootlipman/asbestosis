# Artificial Intelligence-based diagnosis of asbestosis: analysis of a database with applicants for asbestosis state-aid (European Radiology) :computer: :mag_right: 


Managed by Kevin Groot Lipman (k.groot.lipman@nki.nl, k.b.w.grootlipman@gmail.com)

Noninvasive diagnosis of asbestosis for financial compensation suffers from interobserver variability. We developed/integrated an AI-system of multiple components (lung segmentation, anomaly heatmap, classifier) to reproduce the verdict of a panel of medical experts. 

## 1. Setting up the environment :deciduous_tree:
Create and activate a conda environment with Python
 ```
conda create -n asbestosis python
conda activate asbestosis
 ```
Install the requirements (includes R)
 ```
conda install tensorflow-gpu==1.15
conda install keras==2.3.1
conda install pandas
conda install matplotlib==3.2.2
conda install scikit-learn=0.24.1
conda install scipy
pip install pynrrd
 ```
Follow instructions at [link](https://github.com/keras-team/keras-contrib) to install keras_contrib

## 2. How to run the code 🚀 
Download the LIDC-IDRI dataset
Adjust the folders to your own paths in ``data_generator.py`` and ``train.py``. 

You dont need to have anomaly heatmaps or lung segmentations to run it. Just set 'n_channels' in ``train.py`` to 1 and load from your orginal CT folder.

``python train.py``

## 3. Troubleshooting 🔨 
If you encounter a h5py error:
pip install 'h5py==2.10.0' --force-reinstall

## 4. Contribution :muscle:

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated. If you want to add your analysis, or have a suggestion that would make this better, please fork the repo.
