# Training Pipeline – Game-Art Diffusion Model

## Architecture
- Base: Stable Diffusion 1.5 UNet (customized blocks)
- Resolution: 512×512 / 768×768
- Precision: fp16
- Optimization: AdamW + EMA
- Scheduler: Cosine, warmup 500 steps
- Training steps: 200k – 350k

---

## Training Phases

### Phase 1 — Pre-training on stylized silhouettes
Purpose: teach the model strong high-contrast shape structure.

### Phase 2 — Main training on cleaned dataset
Steps: ~150k  
Batch size: 4–8 (depends on VRAM)

### Phase 3 — Style refinement (optional LoRA)
Goal: ensure strong Hollow-Knight-style consistency.

---

## Compute Requirements
### For serious training:
- **A100 40GB**: best balance  
- **RTX 4090 24GB**: minimum viable  
- **H100**: ideal but expensive  

Rough estimate:
- 40–120 GPU hours  
- depends on resolution & dataset size

---

## Output
- final checkpoint (.safetensors)
- inference pipeline
- HuggingFace model card
- sample outputs
