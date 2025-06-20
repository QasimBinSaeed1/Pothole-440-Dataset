# Pothole-440-Dataset

<p align="center">
    <img src="university-of-manitoba-logo.jpg" alt="University of Manitoba" width="320" style="border-radius: 16px; box-shadow: 0 4px 24px rgba(0,0,0,0.15); margin-bottom: 10px;"/>
</p>

<p align="center">
    <b>
        <span style="font-size:1.3em; color:#005DAA;">Department of Civil Engineering</span><br>
        <span style="font-size:1.1em; color:#333;">University of Manitoba</span>
    </b>
</p>

</p>

<p align="center">
    <a href="https://youngjincha.com">youngjincha.com</a>
</p>

---

## Overview

**Pothole-440-Dataset** is a high-quality, curated collection of 440 (1200×800) images capturing diverse pothole scenarios on urban roads. Designed for advanced computer vision research, this dataset supports tasks such as pothole detection, segmentation, and road surface analysis.

---

## Features

- 🎯 **440 Images**: Captured under varied lighting, weather, and road conditions.
- 🏷️ **Annotations**: Includes **binary segmentation masks** for each pothole.
- 📏 **Depth Maps**: High-resolution depth images acquired using Go!SCAN 3D scanner.
- 📁 **Format**: All images in PNG format.
- 🧩 **Use Cases**: Object detection, semantic segmentation, 3D volume estimation, autonomous driving, and infrastructure monitoring.

---

## Dataset Split

| Split   | Images |
|---------|--------|
| Train   | 350    |
| Val     | 50     |
| Test    | 40     |
| **Total** | **440** |

---

## Dataset Structure

```text
Pothole-440-Dataset/
├── annotations/           # COCO and Pascal VOC annotation files
├── test/
│   ├── depth/             # Depth maps (Go!SCAN)
│   ├── mask/              # Binary masks
│   └── rgb/               # RGB images
├── train/
│   ├── depth/
│   ├── mask/
│   └── rgb/
├── val/
│   ├── depth/
│   ├── mask/
│   └── rgb/
└── README.md
```

---

## Getting Started

1. **Clone the repository:**
     ```bash
     git clone https://github.com/QasimBinSaeed1/Pothole-440-Dataset.git
     ```

2. **Explore the data:**
     - RGB images: `rgb/` subfolders in `train/`, `val/`, and `test/`
     - **Binary segmentation masks**: `mask/` subfolders
     - **Depth maps** (Go!SCAN): `depth/` subfolders
     - Annotation files: `annotations/` directory (COCO & Pascal VOC formats)

---

## Example Usage

```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('train/rgb/img_001.png')
mask = cv2.imread('train/mask/img_001.png', 0)
depth = cv2.imread('train/depth/img_001.png', -1)

fig, axs = plt.subplots(1, 3, figsize=(15, 5))
axs[0].imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
axs[0].set_title('RGB Image')
axs[1].imshow(mask, cmap='gray')
axs[1].set_title('Binary Mask')
axs[2].imshow(depth, cmap='plasma')
axs[2].set_title('Depth Map')
for ax in axs: ax.axis('off')
plt.tight_layout()
plt.show()
```

---

## License

This dataset is released under the [CC BY 4.0 License](https://creativecommons.org/licenses/by/4.0/).

---

## Citation

If you use this dataset in your research, please cite:

```bibtex
@article{ali2024monocular,
        title     = {Monocular Computer Vision-Based Simultaneous Pothole Segmentation and 3D Volume Prediction Using 3DPredictNet},
        author    = {Rahmat Ali and Qasim Bin-Saeed and Oral Buyukozturk and SangHyun Lee and YoungJin Cha},
        journal   = {Elsevier},
        year      = {2024},
        note      = {Preprint available at \url{http://dx.doi.org/10.2139/ssrn.5045587}},
        publisher = {Elsevier}
}
```
### Related Research

Ali, R., Bin-Saeed, Q., Buyukozturk, O., Lee, S., & Cha, Y. (2024). *Monocular Computer Vision-Based Simultaneous Pothole Segmentation and 3D Volume Prediction Using 3DPredictNet*. Available at SSRN 5045587. [https://dx.doi.org/10.2139/ssrn.5045587](https://dx.doi.org/10.2139/ssrn.5045587)

## Contact

For questions or collaborations, please contact [binsaeeq@myumanitoba.ca](mailto:binsaeeq@myumanitoba.ca) or [Young.Cha@umanitoba.ca](mailto:Young.Cha@umanitoba.ca).

