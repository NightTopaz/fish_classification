# fish_classification
Download the DeepFish data set from https://cloudstor.aarnet.edu.au/plus/s/NfjObIhtUYO6332/download

Place DeepFish dataset in fishclassification -> src -> datasets

1. Train Single Image

Localization: python scripts/train_single_image.py -e loc -d ${PATH_TO_DATASET}

Segmentation: python scripts/train_single_image.py -e seg -d ${PATH_TO_DATASET}


2. Train and test on the dataset

Run the following command 

python trainval.py -e ${TASK} -sb ${SAVEDIR_BASE} -d ${DATADIR} -r 1

The variables (${...}) can be substituted with the following values:

TASK : loc, seg, clf, reg

SAVEDIR_BASE: Absolute path to where results will be saved

DATADIR: Absolute path containing the downloaded datasets

Experiment hyperparameters are defined in exp_configs.py

Citations

DeepFish Dataset is from:

@article{saleh2020realistic,
    title={A Realistic Fish-Habitat Dataset to Evaluate Algorithms for Underwater Visual Analysis},
    author={Alzayat Saleh and Issam H. Laradji and Dmitry A. Konovalov and Michael Bradley and David Vazquez and Marcus Sheaves},
    year={2020},
    eprint={2008.12603},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}
