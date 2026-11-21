# Digital Image Processing Pipeline

Comprehensive Python implementation of classical **Digital Image Processing** algorithms and visual experiments in Jupyter Notebook (`103` cells), implementing core pixel-level and spatial-domain operations from scratch alongside `scikit-image` and `Pillow`.

---

## Implemented Modules

```mermaid
flowchart LR
    A[Input RGB Images] --> B[Color & Point Ops]
    B --> C[Histogram Analysis]
    C --> D[Spatial Filtering]
    D --> E[Noise Injection]
    E --> F[Morphology & Segmentation]
    F --> G[Floyd-Steinberg Dithering]
```

| Category | Techniques Covered |
|---|---|
| **Color & Point Operations** | Manual RGB-to-Grayscale conversion, brightness addition & multiplication, darkness subtraction & division, multi-image difference subtraction |
| **Histogram Processing** | Manual 256-bin grayscale histogram calculation, contrast histogram stretching, cumulative-distribution histogram equalization |
| **Spatial Filtering** | Mean, Median, Min, Max, Mode, Range, Averaging, Gaussian smoothing, and Laplacian edge-sharpening filters |
| **Noise Modeling** | Salt & Pepper noise, Gaussian noise ($\sigma = 25$), and 2D sinusoidal periodic noise |
| **Morphological Processing** | `5×5` structuring element Dilation, Erosion, Opening, and Closing (`skimage.morphology`) |
| **Segmentation & Halftoning** | Automatic Otsu global thresholding (`filters.threshold_otsu`) and Floyd–Steinberg 1-bit dithering (`PIL.Image.FLOYDSTEINBERG`) |

---

## Repository Structure

```text
.
├── .gitignore
├── README.md
├── requirements.txt
├── assets/
│   └── images/
│       ├── OIP (1).jpg
│       ├── image2.jpg
│       └── image3.jpg
└── notebooks/
    └── image_processing_pipeline.ipynb
```

---

## Getting Started

1. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

2. **Run the notebook**

   - **Google Colab:** Upload `notebooks/image_processing_pipeline.ipynb` and place the 3 sample images from `assets/images/` into `/content/` (the notebook reads `/content/OIP (1).jpg`, `/content/image2.jpg`, and `/content/image3.jpg`).
   - **Local Jupyter:** Launch Jupyter Lab/Notebook and update the image paths in cell 1 if running outside Colab:

     ```bash
     jupyter notebook notebooks/image_processing_pipeline.ipynb
     ```

---

**Author:** Abdelrazek Mohamed Sheta
