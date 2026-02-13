# Bacterial Colony Images on Multiple Media (10-class dataset)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18620619.svg)](https://doi.org/10.5281/zenodo.18620619)

This GitHub repository provides **documentation, metadata, and download instructions** for a bacterial colony image dataset organized by **species × culture medium (10 classes)**. The **full dataset (~9.2 GB)** is archived on **Zenodo** (recommended for research use) under DOI **10.5281/zenodo.18620619**. GitHub may contain a **reduced subset** for quick browsing, but the authoritative release for experiments and citation is the Zenodo archive.

## Download (Full dataset)

- **Zenodo record:** https://zenodo.org/records/18620619  
- **DOI:** https://doi.org/10.5281/zenodo.18620619

Zenodo provides the dataset as ZIP archives (recommended). Use Zenodo for the complete, versioned, citable dataset.

## conversations.jsonl (VLM/VQA supervision layer)

`Description_file/conversations.jsonl` is a **JSON Lines (JSONL)** annotation file where **each line is one JSON record** linking an image (by filename/path that corresponds to the matching file under `Images/...`) to a `conversations` list of natural-language **question–answer pairs** in an instruction/VQA format (e.g., entries like `{ "from": "human", "value": "..." }` and `{ "from": "gpt", "value": "..." }`). This file provides a **machine-readable supervision layer** on top of the raw colony images and can be used to (i) **fine-tune or benchmark vision–language models** for colony interpretation, (ii) build an **interactive QA/teaching assistant** for microbiology lab training, (iii) generate standardized **captions/attribute descriptions** (colour, size range, margin, elevation, texture, opacity, crowding/isolation, purity/contamination cues), and (iv) reproduce prompt/response-based evaluations by grouping records by image and re-running analyses. In short, the images provide visual evidence, while `conversations.jsonl` supplies structured natural-language labels aligned with **species × medium** context for training, retrieval, and evaluation workflows.

## Description File

Description_file/conversations.jsonl is a JSON Lines annotation file (one JSON object per line) that links each colony image to multiple natural-language question–answer pairs in an instruction/VQA format—each record contains an id, an image filename (matching the corresponding file under Images/...), and a conversations array with a human question and an assistant answer (keys like {"from":"human","value":...} and {"from":"gpt","value":...}); in the current subset it includes 16,501 Q/A items covering 592 images, with questions designed to capture colony morphology and diagnostic cues (e.g., colour, size range, margin, elevation, surface texture, opacity), growth/distribution patterns (crowding, isolation suitability, approximate count, purity/contamination hints), and medium-specific indicators (e.g., lactose fermentation cues, EMB sheen, swarming/motility, hemolysis), so it can be used to (i) fine-tune or benchmark vision-language models for colony interpretation, (ii) build an interactive teaching/QA assistant for microbiology lab training, (iii) generate standardized captions/attribute labels for weak supervision, retrieval, or dataset search, and (iv) reproduce the exact prompts/answers used in downstream experiments by grouping records by image and pairing them with the corresponding plate image files in the GitHub subset or Zenodo archive.

## Contact
Tassadaq Hussain
tassadaq@ucerd.com

- **Prof. Dr. Tassadaq Hussain** (corresponding author)  
  Email: tassadaq@ucerd.com
