<div align="center">

# Computer Vision and Generative AI Labs

### From classical image preprocessing to foundation models and diffusion-based generation

*Master's in Artificial Intelligence and Emerging Technologies (MIATE)*
*Faculty of Applied Sciences, Nador - Mohammed First University*

<br/>

![Python](https://img.shields.io/badge/Python-3.10-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-Diffusers-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)

![OCR](https://img.shields.io/badge/OCR-Tesseract-00C853?style=flat-square)
![Grounding DINO](https://img.shields.io/badge/Detection-Grounding%20DINO-0EA5E9?style=flat-square)
![SAM](https://img.shields.io/badge/Segmentation-SAM-00A7E1?style=flat-square)
![Depth Anything](https://img.shields.io/badge/Depth-Depth%20Anything-FF6B6B?style=flat-square)
![Stable Diffusion](https://img.shields.io/badge/Generative%20AI-Stable%20Diffusion-A855F7?style=flat-square)
![ControlNet](https://img.shields.io/badge/Guidance-ControlNet-7C3AED?style=flat-square)
![Labs](https://img.shields.io/badge/Laboratories-3-blue?style=flat-square)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)

</div>

---

## Table of Contents

- [1. Project Overview](#1-project-overview)
- [2. Objectives](#2-objectives)
- [3. Laboratories](#3-laboratories)
  - [3.1. Lab 1: OCR and Image Preprocessing](#31-lab-1-ocr-and-image-preprocessing)
  - [3.2. Lab 2: Object Detection, Segmentation and Depth Estimation](#32-lab-2-object-detection-segmentation-and-depth-estimation)
  - [3.3. Lab 3: Generative AI for Interior Redesign](#33-lab-3-generative-ai-for-interior-redesign)
- [4. Pipeline Summary](#4-pipeline-summary)
- [5. Technologies Used](#5-technologies-used)
- [6. Repository Structure](#6-repository-structure)
- [7. Prerequisites](#7-prerequisites)
- [8. Installation and Execution](#8-installation-and-execution)
- [9. Notes and Limitations](#9-notes-and-limitations)
- [10. Image Credits](#10-image-credits)
- [11. Author](#11-author)

---

## 1. Project Overview

This repository is a collection of three academic laboratories exploring **Computer Vision and Generative AI**. They range from classical image preprocessing and optical character recognition to modern foundation models (Grounding DINO, Segment Anything, Depth Anything) and diffusion-based image generation (Stable Diffusion with ControlNet).

Each experiment is independent yet complementary, implemented in a dedicated Jupyter notebook and documented with its inputs, outputs, and visual results.

| Lab | Focus | Key Technologies |
|---|---|---|
| **1. OCR and Image Preprocessing** | Text extraction from a degraded, noisy image | OpenCV, Tesseract OCR |
| **2. Detection, Segmentation and Depth** | Full scene understanding from a single image | Grounding DINO, SAM, Depth Anything |
| **3. Generative Interior Redesign** | Image-to-image generation with structural guidance | Stable Diffusion, ControlNet |

The progression follows a pedagogical path: from **pixel-level processing** (Lab 1), through **semantic scene analysis** (Lab 2), to **creative image synthesis** (Lab 3).

```mermaid
flowchart LR
    A["Lab 1<br/>Pixel-level processing<br/>OpenCV + Tesseract"] --> B["Lab 2<br/>Semantic scene analysis<br/>Grounding DINO + SAM + Depth Anything"]
    B --> C["Lab 3<br/>Creative image synthesis<br/>Stable Diffusion + ControlNet"]
```

---

## 2. Objectives

The main objectives of the project are as follows:

- Improve OCR accuracy on a difficult image through a rigorous preprocessing pipeline.
- Combine text-prompted detection, mask generation, and monocular depth estimation in a single analysis pipeline.
- Explore diffusion-based image-to-image generation while preserving structural layout via ControlNet.
- Document each experiment reproducibly, with inputs, outputs, and visual comparisons versioned in the repository.

---

## 3. Laboratories

### 3.1. Lab 1: OCR and Image Preprocessing

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Tesseract](https://img.shields.io/badge/Tesseract-OCR-00C853?style=flat-square)

This lab explores image preprocessing techniques designed to improve optical character recognition on a noisy, difficult-to-read image.

**What it covers**

- Grayscale conversion and noise reduction.
- Otsu thresholding and morphological operations.
- Image resizing and border padding.
- Text extraction using an OCR engine.

**Before / After**

| Original image | Processed image |
|:---:|:---:|
| <img src="ex1-ocr/images/original.png" alt="Original degraded image" width="100%"/> | <img src="ex1-ocr/results/output.png" alt="Processed image" width="100%"/> |

**Notebook:** [ocr_preprocessing.ipynb](ex1-ocr/ocr_preprocessing.ipynb)

---

### 3.2. Lab 2: Object Detection, Segmentation and Depth Estimation

![Grounding DINO](https://img.shields.io/badge/Grounding%20DINO-0EA5E9?style=flat-square)
![SAM](https://img.shields.io/badge/Segment%20Anything-00A7E1?style=flat-square)
![Depth Anything](https://img.shields.io/badge/Depth%20Anything-FF6B6B?style=flat-square)

A computer vision pipeline combining three model capabilities to analyze a real-world scene.

**What it covers**

- Detecting objects from a text prompt using Grounding DINO.
- Generating object segmentation masks with SAM.
- Estimating relative scene depth with Depth Anything.
- Visualizing and combining model outputs.

<div align="center">

**Input scene**

<img src="ex3-detection-segmentation-depth/images/input_image.jpeg" alt="Original street scene" width="80%"/>

**Detection and segmentation**

<img src="ex3-detection-segmentation-depth/results/detected_and_segmented.jpeg" alt="Detected and segmented scene" width="80%"/>

**Depth estimation**

<img src="ex3-detection-segmentation-depth/results/Depth_map.png" alt="Estimated scene depth map" width="80%"/>

</div>

**Notebook:** [detection_segmentation_depth.ipynb](ex3-detection-segmentation-depth/detection_segmentation_depth.ipynb)

> **Note:** The depth map represents model-estimated depth. It should not be interpreted as calibrated physical distances without additional validation.

---

### 3.3. Lab 3: Generative AI for Interior Redesign

![Diffusers](https://img.shields.io/badge/Hugging%20Face-Diffusers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![Stable Diffusion](https://img.shields.io/badge/Stable%20Diffusion-A855F7?style=flat-square)
![ControlNet](https://img.shields.io/badge/ControlNet-7C3AED?style=flat-square)

An image-to-image generation workflow that explores how diffusion models can redesign an existing bedroom while using structural guidance to help preserve the room's layout.

**What it covers**

- Preparing an input image and extracting structural edges.
- Conditioning image generation with ControlNet.
- Designing positive and negative prompts.
- Generating and comparing the redesigned image with the original.

<div align="center">

**Before / After comparison**

<img src="ex4-interior-redesign/results/ex4_output_comparaison.png" alt="Original bedroom and AI-generated redesign" width="90%"/>

</div>

| Original image | Generated result |
|:---:|:---:|
| <img src="ex4-interior-redesign/images/input_ex4.jpeg" alt="Original bedroom" width="100%"/> | <img src="ex4-interior-redesign/results/ex4_output_after.png" alt="AI-generated bedroom redesign" width="100%"/> |

**Notebook:** [interior_redesign.ipynb](ex4-interior-redesign/interior_redesign.ipynb)

> **Note:** Generated images may change some original details. ControlNet provides structural guidance but does not guarantee exact preservation.

---

## 4. Pipeline Summary

| Lab | Processing Pipeline |
|---|---|
| **1** | Load, grayscale, noise reduction, Otsu thresholding, morphology, resize and border, OCR |
| **2** | Text prompt, Grounding DINO detection, SAM segmentation masks, Depth Anything estimation, combined visualization |
| **3** | Input image, structural edge extraction, ControlNet conditioning, prompt design, diffusion image-to-image, comparison |

```mermaid
flowchart TB
    subgraph L1["Lab 1: OCR"]
        direction LR
        a1[Load] --> a2[Grayscale] --> a3[Noise reduction] --> a4[Otsu threshold] --> a5[Morphology] --> a6[Resize + border] --> a7[OCR]
    end
    subgraph L2["Lab 2: Scene understanding"]
        direction LR
        b1[Text prompt] --> b2[Grounding DINO] --> b3[SAM masks] --> b4[Depth Anything] --> b5[Combined view]
    end
    subgraph L3["Lab 3: Generation"]
        direction LR
        c1[Input image] --> c2[Edge extraction] --> c3[ControlNet] --> c4[Prompt design] --> c5[Img2img diffusion] --> c6[Comparison]
    end
```

---

## 5. Technologies Used

| Technology | Usage |
|---|---|
| Python | Main project language |
| Jupyter Notebook | Interactive development and execution of each lab |
| OpenCV | Image preprocessing, morphology, resizing, and padding (Lab 1) |
| Tesseract OCR (PyTesseract) | Optical character recognition (Lab 1) |
| Grounding DINO | Open-vocabulary object detection from text prompts (Lab 2) |
| Segment Anything (SAM) | Generation of object segmentation masks (Lab 2) |
| Depth Anything | Monocular depth estimation (Lab 2) |
| Hugging Face Diffusers | Diffusion model orchestration (Lab 3) |
| Stable Diffusion + ControlNet | Image-to-image generation with structural guidance (Lab 3) |

---

## 6. Repository Structure

```text
computer-vision-and-generative-ai-labs/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── ex1-ocr/
│   ├── ocr_preprocessing.ipynb
│   ├── images/
│   │   └── original.png
│   └── results/
│       └── output.png
│
├── ex3-detection-segmentation-depth/
│   ├── detection_segmentation_depth.ipynb
│   ├── images/
│   │   └── input_image.jpeg
│   └── results/
│       ├── detected_and_segmented.jpeg
│       └── Depth_map.png
│
└── ex4-interior-redesign/
    ├── interior_redesign.ipynb
    ├── images/
    │   └── input_image_ex4.jpeg
    └── results/
        ├── ex4_output_after.png
        └── ex4_output_comparaison.png
```

---

## 7. Prerequisites

To run the laboratories, the following elements are required:

- Python 3.10 or a compatible version for the selected library versions.
- Jupyter Notebook.
- Dependencies listed in `requirements.txt`.
- Tesseract OCR installed separately at the system level (Lab 1).
- Additional model dependencies and checkpoints for Labs 2 and 3.

---

## 8. Installation and Execution

### 8.1. Project Retrieval

Clone the Git repository:

```bash
git clone https://github.com/mohammed-boujaada/computer-vision-and-generative-ai-labs.git
cd computer-vision-and-generative-ai-labs
```

### 8.2. Environment Setup

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

### 8.3. Notebook Execution

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open the notebook corresponding to the lab you want to explore and execute the cells in order.

### 8.4. Additional Setup per Lab

| Lab | Additional setup |
|---|---|
| **Lab 1** | Install the Tesseract OCR executable for your operating system. The `pytesseract` Python package acts as an interface to it. |
| **Lab 2** | Download the required model checkpoints and follow the setup instructions in the notebook. The SAM checkpoint is not included in this repository. |
| **Lab 3** | The diffusion models and ControlNet weights may require substantial disk space, RAM, and GPU memory. Follow the notebook's model-loading instructions. |

Exact compatibility and resource requirements depend on the Python environment, library versions, models, and available hardware.

---

## 9. Notes and Limitations

- These notebooks present selected academic implementations and experiments.
- Results may vary depending on library versions, model checkpoints, hardware, and input images.
- Model weights and large checkpoints are not included in the repository.
- Use images and model checkpoints according to their licenses and usage terms.

---

## 10. Image Credits

Some images used in these labs were sourced from Google Images for educational and demonstration purposes. All rights belong to their respective owners.

---

## 11. Author

<div align="center">

<table>
<tr>
<td align="center" width="280">
<a href="https://github.com/mohammed-boujaada">
<img src="https://github.com/mohammed-boujaada.png" width="120px" alt="Mohammed Boujaada"/>
<br/>
<sub><b>Mohammed Boujaada</b></sub>
</a>
<br/>
MIATE Master's, FSA Nador
<br/><br/>
<a href="https://github.com/mohammed-boujaada">
<img src="https://img.shields.io/badge/GitHub-@mohammed--boujaada-181717?style=flat-square&logo=github"/>
</a>
<br/>
<a href="https://www.linkedin.com/in/mohammed-boujaada-229a3333a/">
<img src="https://img.shields.io/badge/LinkedIn-Mohammed%20Boujaada-0A66C2?style=flat-square&logo=linkedin&logoColor=white"/>
</a>
</td>
</tr>
</table>

<br/>

| | |
|---|---|
| **Institution** | FSA Nador, Master's in Artificial Intelligence and Emerging Technologies |
| **Module** | Computer Vision and Generative AI |
| **Academic Year** | 2025 - 2026 |

</div>
