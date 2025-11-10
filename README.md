# Deep-Learning-Radiomic-Stability
This repository contains all the code for my paper "Radiomic Stability and Segmentation Performance of Six Deep Learning Models for Ovarian Tumor Ultrasound Images."

**Abstract**
Recent advances in deep learning have produced highly robust and efficient models for medical image segmentation. Despite this, few studies assess the **radiomic stability **of these state-of-the-art approaches for applications in ovarian tumor segmentation. This study compared six deep learning architectures with unique backbones by evaluating their performance and radiomic stability on 1469 two-dimensional (2D) ultrasound images from the Multi-Modality Ovarian Tumor Ultrasound (MMOTU) dataset. The tested models were U-Net++, DeepLabV3+, U-Net, SegFormer, FPN, and LinkNet. Standard performance was assessed using Dice and IoU scores, precision, recall, specificity, size error, and 95th percentile Hausdorff distance (HD95). Radiomic stability evaluation involved extracting 102 quantitative features, followed by a Pearson correlation analysis between the predicted and ground truth masks. All models performed well, with average Dice scores of 0.9311, 0.9259, 0.9277, 0.9271, 0.9280, and 0.9213 for U-Net++, DeepLabV3+, U-Net, SegFormer, FPN, and LinkNet, respectively. Radiomic correlations were similarly high, ranging from 0.9400 to 0.9518. Small but significant differences were observed across models (p < 0.05). U-Net++ achieved the best Dice and IoU scores, precision, HD95, and size error, while SegFormer obtained the strongest radiomic stability. These results provide a comparative benchmark for ovarian tumor segmentation, underscoring how model choice can influence mask quality and radiomic stability.

**Dataset**

All data was obtained from the Multi-Modality Ovarian Tumor Ultrasound (MMOTU) dataset. The original study can be found below: 

Zhao Q, Lyu S, Bai W, Cai L, Liu B, Cheng G, Wu M, Sang X, Yang M, Chen L (2022) A multi-modality ovarian tumor ultrasound image dataset for unsupervised cross-domain semantic segmentation. CoRR, vol. abs/2207.06799

**Software**

All training and model development were completed using the following tools and libraries: 
- Google Colab using Python 3.11.13 with a T4 GPU 
- Matplotlib 3.10.0 and Seaborn 0.13.2 for data visualization,
- Qubvel’s Segmentation Models Pytorch 0.5.1.dev0 GitHub repository and PyTorch 2.0.1 for constructing the six deep learning models
- Pyradiomics v3.0.1 for radiomic extraction
- Pillow (PIL) 11.3.0 and cv2 4.12.0 for image and mask handling/ preprocessing
- Scikit-posthocs 0.11.4 and SciPy 1.16.1 for statistical analysis
