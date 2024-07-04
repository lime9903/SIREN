# SIREN

## Requirements

First, install the requirements of the system.

```bash
sudo pip install -r requirements.txt
```

An easy installation if you already have Python 3 and CUDA 9.0:

```bash
conda install pytorch=0.4.1
pip install cython
pip install matplotlib numpy scipy pyyaml packaging pycocotools tensorboardX tqdm pillow scikit-image gensim
conda install opencv
```

## Directory Structure

The final directories for data and detection models should look like:

```bash
|-- detection_models
|   |-- vg
|   |   |-- VGG16
|   |   |   |-- model_step479999.pth
|   |   |-- X-101-64x4d-FPN
|   |   |   |-- model_step119999.pth
|   |-- vrd
|   |   |-- VGG16
|   |   |   |-- model_step4499.pth
|-- data
|   |-- vg
|   |   |-- VG_100K    <-- (contains Visual Genome all images)
|   |   |-- rel_annotations_train.json
|   |   |-- rel_annotations_val.json
|   |   |-- ...
|   |-- vrd
|   |   |-- train_images    <-- (contains Visual Relation Detection training images)
|   |   |-- val_images    <-- (contains Visual Relation Detection validation images)
|   |   |-- new_annotations_train.json
|   |   |-- new_annotations_val.json
|   |   |-- ...
|   |-- word2vec_model
|   |   |-- GoogleNews-vectors-negative300.bin
|-- trained_models
|   |-- e2e_relcnn_VGG16_8_epochs_vg_y_loss_only
|   |   |-- model_step125445.pth
|   |-- e2e_relcnn_X-101-64x4d-FPN_8_epochs_vg_y_loss_only
|   |   |-- model_step125445.pth
|   |-- e2e_relcnn_VGG16_8_epochs_vrd_y_loss_only
|   |   |-- model_step7559.pth
|   |-- e2e_relcnn_VGG16_8_epochs_vrd_y_loss_only_w_freq_bias
|   |   |-- model_step7559.pth
```

