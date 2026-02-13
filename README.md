# Bacterial Colony Images on Multiple Media (10-class dataset)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18620619.svg)](https://doi.org/10.5281/zenodo.18620619)

This GitHub repository provides **documentation, metadata, and download instructions** for a bacterial colony image dataset organized by **species × culture medium (10 classes)**. The **full dataset (~9.2 GB)** is archived on **Zenodo** (recommended for research use) under DOI **10.5281/zenodo.18620619**. GitHub may contain a **reduced subset** for quick browsing, but the authoritative release for experiments and citation is the Zenodo archive.

## Download (Full dataset)

- **Zenodo record:** https://zenodo.org/records/18620619  
- **DOI:** https://doi.org/10.5281/zenodo.18620619

Zenodo provides the dataset as ZIP archives (recommended). Use Zenodo for the complete, versioned, citable dataset.

## conversations.jsonl (VLM/VQA supervision layer)

`Description_file/conversations.jsonl` is a **JSON Lines (JSONL)** annotation file where **each line is one JSON record** linking an image (by filename/path that corresponds to the matching file under `Images/...`) to a `conversations` list of natural-language **question–answer pairs** in an instruction/VQA format (e.g., entries like `{ "from": "human", "value": "..." }` and `{ "from": "gpt", "value": "..." }`). This file provides a **machine-readable supervision layer** on top of the raw colony images and can be used to (i) **fine-tune or benchmark vision–language models** for colony interpretation, (ii) build an **interactive QA/teaching assistant** for microbiology lab training, (iii) generate standardized **captions/attribute descriptions** (colour, size range, margin, elevation, texture, opacity, crowding/isolation, purity/contamination cues), and (iv) reproduce prompt/response-based evaluations by grouping records by image and re-running analyses. In short, the images provide visual evidence, while `conversations.jsonl` supplies structured natural-language labels aligned with **species × medium** context for training, retrieval, and evaluation workflows.

## Notes on GitHub hosting

GitHub has strict limits for large repositories; in particular, a **single git push is limited to 2 GiB**, and very large files are discouraged. For research-grade distribution, please use Zenodo (DOI above). If a lightweight subset is provided via GitHub, it may be distributed as **Release assets** (ZIPs) to keep the repository itself small.

## Contact

- **Prof. Dr. Tassadaq Hussain** (corresponding author)  
  Email: tassadaq@ucerd.com
