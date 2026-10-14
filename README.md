# Computer Vision Labs

A collection of selected academic labs exploring **Computer Vision and Generative AI** using Python, OpenCV, OCR, modern vision models, and diffusion-based image generation.

The repository covers image preprocessing, text recognition, object detection, image segmentation, monocular depth estimation, and AI-powered interior redesign.

## Labs

### 1. OCR and Image Preprocessing

**Technologies:** Python · OpenCV · Tesseract OCR

This lab explores image preprocessing techniques to improve OCR on a noisy, difficult-to-read image.

**What it covers**
- Grayscale conversion and noise reduction.
- Otsu thresholding and morphological operations.
- Image resizing and border padding.
- Text extraction using an OCR engine.

| Original image | Processed image |
|---|---|
| ![Original OCR image](ex1-ocr/images/original.png) | ![Processed OCR image](ex1-ocr/results/output.png) |

**Notebook:** [ocr_preprocessing.ipynb](ex1-ocr/ocr_preprocessing.ipynb)

---

### 2. Object Detection, Segmentation and Depth Estimation

**Technologies:** Python · Grounding DINO · Segment Anything (SAM) · Depth Anything

A computer vision pipeline combining three model capabilities to analyze a real-world scene.

**What it covers**
- Detecting objects from a text prompt using Grounding DINO.
- Generating object segmentation masks with SAM.
- Estimating relative scene depth.
- Visualizing and combining model outputs.

**Input scene**

![Original street scene](ex3-detection-segmentation-depth/images/input_image.jpg)

**Detection and segmentation**

![Detected and segmented scene](ex3-detection-segmentation-depth/results/detected_and_segmented.png)

**Depth estimation**

![Estimated scene depth map](ex3-detection-segmentation-depth/results/depth_map.png)

**Notebook:** [detection_segmentation_depth.ipynb](ex3-detection-segmentation-depth/detection_segmentation_depth.ipynb)

*Note: The depth map represents model-estimated depth. It should not be interpreted as calibrated physical distances without additional validation.*

---

### 3. Generative AI for Interior Redesign

**Technologies:** Python · Hugging Face Diffusers · Stable Diffusion · ControlNet

An image-to-image generation workflow that explores how diffusion models can redesign an existing bedroom while using structural guidance to help preserve the room's layout.

**What it covers**
- Preparing an input image and extracting structural edges.
- Conditioning image generation with ControlNet.
- Designing positive and negative prompts.
- Generating and comparing the redesigned image with the original.

**Before and after**

![Original bedroom and AI-generated redesign](ex4-interior-redesign/results/ex4_output_comparaison.png)

**Generated result**

![AI-generated bedroom redesign](ex4-interior-redesign/results/ex4_output_after.png)

**Original image**

![Original bedroom](ex4-interior-redesign/images/input_image_ex4.jpg)

**Notebook:** [interior_redesign.ipynb](ex4-interior-redesign/interior_redesign.ipynb)

*Note: Generated images may change some original details. ControlNet provides structural guidance but does not guarantee exact preservation.*

---

## Repository Structure

```text
computer-vision-labs/
├── README.md
├── requirements.txt
├── .gitignore
├── ex1-ocr/
│   ├── ocr_preprocessing.ipynb
│   ├── images/
│   │   └── original.png
│   └── results/
│       └── output.png
├── ex3-detection-segmentation-depth/
│   ├── detection_segmentation_depth.ipynb
│   ├── images/
│   │   └── input_image.jpg
│   └── results/
│       ├── detected_and_segmented.png
│       └── depth_map.png
└── ex4-interior-redesign/
    ├── interior_redesign.ipynb
    ├── images/
    │   └── input_image_ex4.jpg
    └── results/
        ├── ex4_output_after.png
        └── ex4_output_comparaison.png
```

## Getting Started

### Requirements

- Python 3.10 or a compatible version for the selected library versions.
- Jupyter Notebook.
- Dependencies listed in `requirements.txt`.
- Tesseract OCR installed separately for Ex1.
- Additional model dependencies and checkpoints for Ex3 and Ex4.

### Installation

Clone the repository:

```bash
git clone https://github.com/moza369/computer-vision-labs.git
cd computer-vision-labs
```

Create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

On Windows, activate it using:

```powershell
.venv\Scripts\activate
```

Install the dependencies:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
python -m pip install notebook
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook corresponding to the lab you want to explore.

### Additional Setup

- **Ex1:** Install the Tesseract OCR executable for your operating system. The `pytesseract` Python package acts as an interface to it.
- **Ex3:** Download the required model checkpoints and follow the setup instructions in the notebook. The SAM checkpoint is not included in this repository.
- **Ex4:** The diffusion models and ControlNet weights may require substantial disk space, RAM, and GPU memory. Follow the notebook's model-loading instructions.

Exact compatibility and resource requirements depend on the Python environment, library versions, models, and available hardware.

## Notes

- These notebooks present selected academic implementations and experiments.
- Results may vary depending on library versions, model checkpoints, hardware, and input images.
- Model weights and large checkpoints are not included in the repository.
- Use images and model checkpoints according to their licenses and usage terms.


## Image Credits

Some images used in these labs were sourced from Google Images for educational and demonstration purposes. All rights belong to their respective owners.

## Author

**Mohamed Zahir**

Master's student in Artificial Intelligence and Emerging Technologies, interested in AI Engineering, Computer Vision, Generative AI, and AI Security.

- GitHub: [moza369](https://github.com/moza369)
- Portfolio: [moza369.github.io](https://moza369.github.io/)
