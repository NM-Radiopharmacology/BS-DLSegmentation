# BS-DLSegmentation

Fully automatic deep learning models for segmenting bone metastases in both **anterior and posterior projections of whole-body bone scintigraphies**.

---

## Table of Contents
- [Prerequisites & Installation](#prerequisites--installation)
- [Model Weights](#model-weights)
- [Data Preparation](#data-preparation)
- [Inference](#inference)
- [Contact & Citation](#contact--citation)

---

## Prerequisites & Installation

This project relies on the **nnU-Net** framework. Ensure you have installed all necessary dependencies and properly configured the required nnU-Net environment variables (`nnUNet_raw_data_base`, `nnUNet_preprocessed`, `RESULTS_FOLDER`).

Refer to the official [nnU-Net Installation Guide](https://github.com/MIC-DKFZ/nnUNet) for detailed instructions.

---

## Model Weights

Pre-trained model weights are required to run inference.

* **Download Link:** [LINK OR FOLDER]
* **Setup:** Place the downloaded weights into your designated `RESULTS_FOLDER` following standard nnU-Net folder structure.

---

## Data Preparation

>> RIGHT???? 

Input images must be in **NIfTI (`.nii.gz`)** format and follow the nnU-Net naming convention (`<patientID>_<channel>.nii.gz`):

* `patientID_0000.nii.gz`: Anterior projection
* `patientID_0001.nii.gz`: Posterior projection

> **Note:** If your input formats or channels differ, adjust the channel indices (`_0000`, `_0001`) to match your training setup.

---

## Inference

Run prediction from the terminal by pointing to your input data directory (`PATH_INPUT`) and target output directory (`PATH_OUTPUT`):

```bash
nnUNet_predict -i /path/to/PATH_INPUT -o /path/to/PATH_OUTPUT -t 1
```

## Contact & Support

If you need help with data preparation, environment setup, or running inference:
- **Email:** [francisco.oliveira@fundacaochampalimaud.pt](mailto:francisco.oliveira@fundacaochampalimaud.pt)
- **Issues:** Feel free to open an issue in this repository.
