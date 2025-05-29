# CEDNAV–UTB: Efficient Image Retrieval for Arguments with CLIP

<img src="https://github.com/user-attachments/assets/44305bf0-c24a-4c1d-8f87-852445707970" width="150" alt="Firma animada">      
<img src="https://github.com/user-attachments/assets/4c167b85-1fb9-4f8d-8ef9-9e0d60cf01c7" width="250" alt="Firma animada">     
<img src="https://github.com/user-attachments/assets/1658fa2f-d8a3-494f-a812-fc33cf471188" width="350" alt="Firma animada">

## This repository contains the official implementation developed by the UTB–CEDNAV team for the Image Retrieval for Arguments task at [Touché 2025](https://touche.webis.de/clef25/touche25-web/image-retrieval-for-arguments.html). The solution offers a simple, sustainable, and reproducible baseline for matching textual arguments with relevant images using CLIP (ViT-B/32).

## Overview
The system focuses on retrieving—not generating—images that are semantically aligned with argument claims. It leverages CLIP to compute textual embeddings for both argument claims and image captions, then ranks images by cosine similarity. Unlike many prior approaches, it avoids OCR, re-rankers, or generative models, minimizing technical dependencies and reducing computational load.

## Key Features
```bash
🔍 CLIP-based text-to-text retrieval between argument claims and image captions
⚡ High computational efficiency via parallel processing and embedding reuse
🌱 Low environmental impact, measured and tracked using CodeCarbon
🧪 Valid output for the official Touché 2025 validator and format (submission.jsonl)
☁️ Google Colab-ready for scalable and accessible deployment
```

## System Highlights
Dataset: Uses the official Touché 2025 dataset (XML and image-caption pairs)
Embeddings: Precomputes and reuses CLIP embeddings for both claims and captions
Similarity Computation: Ranks images per claim using cosine similarity
Output Format: Produces submission.jsonl compatible with Touché 2025 evaluation tools
Sustainability: Achieves over 85% reduction in CO₂ emissions in subsequent runs by avoiding redundant computations

## Getting Started
To replicate the experiments:

1. Clone the repository and open the Colab notebook.

Note: Click the badge below to launch the notebook directly in Google Colab:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/11HhJJcfZ87bkSmhzJzU32SjK8EbND57D?usp=sharing)


3. Mount your Google Drive and ensure it includes:
  - [Download arguments.xml](https://zenodo.org/records/15123526/files/arguments.xml?download=1)
  - [Download touche25-image-retrieval-and-generation-main.zip](https://zenodo.org/records/15123526/files/touche25-image-retrieval-and-generation-main.zip?download=1)
    
3. Run the pipeline end-to-end:
  - Extract the dataset
  - Load and embed captions and claims
  - Compute similarities and generate the output
4. Use the official validator to verify the results

## Repository Structure
```bash
TOUCHE_2025/
├── touché2025_v7.py           # Main script with full retrieval pipeline
├── CEDNAV_UTB_paper.pdf       # Working Notes paper submitted to CLEF 2025
├── submission.jsonl           # submission
└── README.md                  # This file
```


## Citation
- Heinrich, M., Kiesel, J., Wolter, M., Potthast, M., & Stein, B. (2025). Touché-Argument-Images | ImageCLEF / LifeCLEF - Multimedia Retrieval in CLEF [Online]. Available at: https://www.imageclef.org/2025/argument-images (Accessed May 26, 2025)
- Heinrich, M., Kiesel, J., Wolter, M., Potthast, M., & Stein, B. (2025). Touché25-Image-Retrieval-and-Generation-for-Arguments [Dataset]. Zenodo. https://doi.org/10.5281/zenodo.15123526 (Accessed May 26, 2025)
- Lacoste, A., Luccioni, S., Schmidt, V., & Dandres, T. (2021). CodeCarbon: Estimate the carbon footprint of your compute usage [Software]. GitHub. https://doi.org/10.5281/zenodo.5105071 (Accessed May 26, 2025)


## Contact
Team: Computer Vision UTB
Affiliation: CEDNAV – Naval Technological Development Center, Colombian Navy
Country: Colombia
Contact Person: Diego Guevara
Email: hiperdaga7@gmail.com

