# LoRA Fine-tuning (4-bit) — French Spelling Correction (Kaggle 2×T4)

This repo contains an end-to-end notebook to fine-tune an instruction-tuned LLM for **Spelling correction** using **LoRA** (PEFT) with **4-bit quantization**.  
Training was run on **Kaggle** using **2× NVIDIA T4 GPUs**.

**Pipeline:** data → prompt formatting → loss masking → LoRA fine-tuning → evaluation (EM/CER) → inference → save adapter

---

## Highlights
- **Parameter-efficient fine-tuning (LoRA)** + **4-bit** loading for low VRAM usage
- **Instruction-style prompts** (Input → Response)
- **Loss masking** to train only on the `### Response:` part (target text)
- Simple evaluation: **Exact Match (EM)** and **Character Error Rate (CER)**

---

## Results (fill in)
| Model | Exact Match (EM) | CER (↓) |
|------|-------------------|---------|
| Base model | 0.002  | 0.334 |
| Fine-tuned (LoRA) | 0.260  | 0.109 |


## Dataset
This project uses the Kaggle dataset **“spelling-mistake-data-1mn”**.


### Kaggle
1. Create a Kaggle notebook
2. Add the dataset as an input
3. Run `notebooks/finetune_lora_spellcheck.ipynb`
