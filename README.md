# Pothole-440-Dataset
  

## Overview

**Pothole-440-Dataset** is a curated collection of 440 (1200*800) images capturing diverse pothole scenarios on urban roads. This dataset is designed for research and development in computer vision tasks such as pothole detection, segmentation, and road surface analysis.

## Features

- **440 Images**: Diverse lighting, weather, and road conditions.
- **Annotations**: Bounding boxes and segmentation masks for each pothole.
- **Format**: Images in JPEG/PNG, annotations in COCO and Pascal VOC formats.
- **Use Cases**: Object detection, semantic segmentation, autonomous driving, infrastructure monitoring.

## Dataset Structure

```
Pothole-440-Dataset/
├── test/
│   ├── depth
│   │   ├── img_001.png
│   │   └── ...
│   ├── mask
│   │   ├── img_001.png
│   │   └── ...
│   └── rgb
│       ├── img_001.png
│       └── ...
├── train/
│   ├── depth
│   │   ├── img_001.png
│   │   └── ...
│   ├── mask
│   │   ├── img_001.png
│   │   └── ...
│   └── rgb
│       ├── img_001.png
│       └── ...
├── val/
│   ├── depth
│   │   ├── img_001.png
│   │   └── ...
│   ├── mask
│   │   ├── img_001.png
│   │   └── ...
│   └── rgb
│       ├── img_001.png
│       └── ...
└── README.md
```

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/QasimBinSaeed1/Pothole-440-Dataset.git
   ```

3. **Explore the data:**
- Images are located in the `rgb/` subfolders within `train/`, `val/`, and `test/`.
- Segmentation masks are in the corresponding `mask/` subfolders.
- Depth maps are available in the `depth/` subfolders.
- Each split (`train`, `val`, `test`) maintains the same folder structure.
- Annotation files in COCO and Pascal VOC formats are provided in the `annotations/` directory.

## Example Usage

```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('images/img_001.png')
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title('Sample Pothole Image')
plt.show()
```

## License

This dataset is released under the [CC BY 4.0 License](https://creativecommons.org/licenses/by/4.0/).

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
}
```

## Contact

For questions or collaborations, please contact [binsaeeq@myumanitoba.ca](mailto:binsaeeq@myumanitoba.ca) or [Young.Cha@umanitoba.ca](mailto:Young.Cha@umanitoba.ca).
