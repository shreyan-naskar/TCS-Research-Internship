# ISLR

Notebook work for Indian Sign Language Recognition experiments completed as part of the TCS Research Internship.

## Contents

| Path         | Description                                                        |
| ------------ | ------------------------------------------------------------------ |
| `main.ipynb` | Main notebook for Indian Sign Language Recognition experimentation |

## Notebook Overview

The notebook focuses on a Video Mamba based action-recognition workflow for sign-language video classification. It includes environment setup, model dependency checks, dataset split preparation, training-related configuration, and metric visualization.

The workflow includes:

1. Preparing train, validation, and test CSV files from class-organized video folders.
2. Loading a pretrained Kinetics-400 checkpoint from the Video Mamba Suite model zoo.
3. Adapting the model head for the target ISLR classes.
4. Running or inspecting training output.
5. Parsing logged metrics and plotting training progress.

## Expected Environment

The notebook uses Python with PyTorch and Video Mamba related dependencies, including `causal_conv1d`, `mamba_ssm`, `timm`, NumPy, and Matplotlib.

Some paths inside the notebook are machine-specific and should be updated before running on a new system, especially dataset paths, checkpoint paths, and output log paths.

## Running

1. Open `main.ipynb`.
2. Update local dataset, checkpoint, and output paths where needed.
3. Run the setup and dependency-check cells.
4. Generate the train, validation, and test CSV files.
5. Run the training or evaluation cells.
6. Review the parsed metrics and plots near the end of the notebook.
