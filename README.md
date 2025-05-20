# 🍎 Pomegranate Disease Classification Using Advanced Deep Learning Models

This repository contains the code and experiments for the research project titled **"Pomegranate Disease Classification Using Advanced Deep Learning Models"**, accepted for publication at the 2025 IEEE 4th International Conference on Computing and Machine Intelligence (ICMI).

Our goal was to evaluate multiple deep learning architectures for classifying pomegranate fruit diseases using high-resolution images. We compare the performance, efficiency, and portability of three advanced models to determine their real-world deployment potential, particularly for mobile and drone-based platforms.

## 📌 Abstract

Pomegranate crops are susceptible to a variety of diseases that can drastically impact yield and quality. Traditional detection techniques are often labor-intensive and inefficient. This study applies modern deep learning techniques to automatically detect and classify diseases in pomegranate fruits using image data.

We trained and evaluated the following models:
- **DaViT-Base** (Transformer-based)
- **EfficientNetV2-M** (CNN optimized for performance)
- **MobileOne-S4** (Lightweight CNN for edge deployment)

All models achieved **over 99% classification accuracy**, with EfficientNetV2-M offering the best trade-off between performance and training time, and MobileOne-S4 excelling in portability for mobile use.

## 📁 Project Structure
```text
📦pomegranate-disease-classification/
┣ 📂notebooks/ # Jupyter notebooks with experiments and results
┣ 📂models/final # Model architectures and training scripts
┣ 📜README.md # You're here
┗ 📜requirements.txt # Environment dependencies
```


## 🖼 Dataset

- **Name:** Pomegranate Fruit Diseases Dataset for Deep Learning Models  
- **Source:** Pakruddin, B; Dr. Hemavathy, R. (2023)  
- **Format:** JPEG, 3120x3120 resolution, 5 classes (Alternaria, Anthracnose, Bacterial Blight, Cercospora, Healthy)  
- **License:** [Mendeley Data, V1](https://doi.org/10.17632/b6s2rkpmvh.1)

> **Citation:**
> Pakruddin, B; Hemavathy, R. (2023), “Pomegranate Fruit Diseases Dataset for Deep Learning Models”, Mendeley Data, V1, doi: [10.17632/b6s2rkpmvh.1](https://doi.org/10.17632/b6s2rkpmvh.1)

Note: The full dataset is not uploaded to this repository due to its size. Please download it directly from the source above.

## 🧪 Methodology

- Preprocessing: image resizing (224×224), normalization, and data augmentation.
- Transfer Learning: pretrained weights from ImageNet-21K.
- Training Setup:
  - Optimizer: Adam
  - Loss: Cross-Entropy
  - Scheduler: ReduceLROnPlateau

## 📊 Results

All three models were evaluated using precision, recall, and F1 scores across all five classes. Results showed:

| Model          | Accuracy | Notes                          |
|----------------|----------|--------------------------------|
| DaViT-Base     | 99.2%    | Most complex, slowest training |
| EfficientNetV2 | 99.4%    | Best performance overall       |
| MobileOne-S4   | 99.1%    | Best for edge deployment       |

## 🔗 Download Pretrained Models

Due to GitHub's file size restrictions, the final model weights used in this research are hosted externally:

- [DaViT-Base (Epoch 28)](https://drive.google.com/file/d/1zx3drhG4kYe5cwfDlqgOW5c6ZnoxsBDC/view?usp=sharing&export=download)
- [EfficientNetV2-M (Epoch 27)](https://drive.google.com/file/d/1GbGT-FwZxEfFfXQfYm6V3LyKU45n04YT/view?usp=sharing&export=download)
- [MobileOne-S4 (Epoch XX)](https://drive.google.com/file/d/1lpMx9Lb6XXvaKtIhjSNTtDxuywllNWdk/view?usp=sharing&export=download)

To use these models:

1. Download the `.pth` files and place them in the `models/final/` directory.
2. Ensure the file names match those referenced in the code.

```bash
models/
└── final/
    ├── DaViT_Base_Epoch_28.pth
    ├── EfficientNet_M_Epoch_27.pth
    └── MobileOne_S4_Epoch_31.pth
```

## 🛠 Installation

To run the code:

```bash
git clone https://github.com/your-username/pomegranate-disease-classification.git
cd pomegranate-disease-classification
pip install -r requirements.txt
```

Jupyter Notebooks canbe run using:
```bash
jupyter lab
```

## 🧪 Inference Demo

To test the trained DaViT-Base model on an image, run the following notebook:

[`notebooks/inference_demo_davit.ipynb`](notebooks/inference_demo_davit.ipynb)

This demo:
- Uses the final saved model (`DaViT_Base_Epoch_28.pth`)
- Applies preprocessing consistent with training
- Outputs the predicted class and displays the input image

> 🔄 Replace `sample.jpg` with your own image to test.


## 📄 Citation
This work has been accepted for publication at the 2025 IEEE ICMI.

⚠️ Note: This repository includes the code and research artifacts only. The full paper will be available on IEEE Xplore after publication. Please cite the official paper when using this work.