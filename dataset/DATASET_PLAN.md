# Dataset Plan – Stylized 2D Game-Art Diffusion Model

## Overview
The dataset will focus on stylized 2D game art inspired by Hollow Knight aesthetics:
- thick outlines  
- flat shading  
- muted palettes  
- high-contrast silhouettes  
- hand-drawn texture feel  

The model will learn:
- characters  
- enemies / bosses  
- poses  
- environment tiles  
- props  
- VFX frames (slashes, particles, magic)

---

## Dataset Stages

### 1. Collection (Phase 1)
Sources:
- Public domain art (OpenGameArt)
- CC0 sprite sheets
- Hand-made sketches (generated or drawn)
- Procedurally created silhouettes
- LORA-augmented variants to increase diversity

Target size: **3,000 – 8,000 images**

All images resized to **512×512** or **768×768**.

---

### 2. Cleaning (Phase 2)
Automated scripts will:
- remove backgrounds  
- standardize palette  
- normalize contrast  
- fix transparency issues  
- remove non-stylized/out-of-theme images  

Tools:
- Python + PIL  
- RemBG or custom background mask  
- Image hashing for duplicates  

---

### 3. Annotation (Phase 3)
Not text annotations.  
Instead:
- class tags ("enemy", "boss", "blade", "character", etc)
- style tags ("outline-heavy", "flat-shaded", "dark-palette")

---

### 4. Final Dataset Format
dataset/
raw/
cleaned/
annotations.json
preview_grid.png

---

## Why This Dataset Matters
There is currently **no open-source dataset** focusing on stylized Hollow-Knight-like art for indie developers.  
This dataset enables:
- consistent art style  
- game-ready assets  
- low-VRAM fine-tuning possibilities  
- open-source alternatives to paid asset packs
