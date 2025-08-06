# 📚 Storybook Visions: Text-to-Image Adventures for Kids’ Imagination

**Author:** Praveen Vemasani  
**Email:** pr916703@ucf.edu  
**University of Central Florida, Orlando, FL, USA**  

---

## 🌟 Overview

**Storybook Visions** is an AI-powered project that brings children’s stories to life by generating whimsical illustrations from textual prompts. The goal is to foster imagination and engagement in young readers by transforming narrative descriptions into vibrant, age-appropriate visuals using cutting-edge generative models.

This repository includes:
- Benchmarking of state-of-the-art text-to-image models
- A custom fine-tuning pipeline using DreamBooth + LoRA on Stable Diffusion XL
- A curated multiverse dataset of storybook-style images with handcrafted captions
- Evaluation using CLIP Score, ITI Similarity, and human preference studies

---

## 🧠 Motivation

With increased screen time and passive content consumption, children today are less likely to visualize stories actively. This project explores how generative AI can reinvigorate imagination and storytelling by automatically generating high-quality, narrative-aligned illustrations — reducing the burden on authors and educators.

---

## 🎨 Dataset: The Fantasy Multiverse

25 handcrafted image-caption pairs were created across five fantasy themes:

- 🧙 Wizards  
- 🐉 Dragons  
- 👑 Princesses  
- 🌿 Nature Scenes  
- 🌈 Scene Transitions  

All captions are written in a classic storybook tone to match children's literature aesthetics.

---

## 🛠️ Project Architecture

### Phase I — Benchmarking

Evaluated baseline performance of:
- **Stable Diffusion XL**
- **Dreamlike Diffusion**
- **OpenAI DALL·E**
- **Disney-Pixar Cartoon Diffusion**
- **Janus-Pro-7B & 1B (DeepSeek)**

Metrics used:
- `CLIP Score` for text-image alignment  
- `ITI Similarity` for semantic depth  
- Human reviews for aesthetics and creativity

---

### Phase II — Fine-Tuning Pipeline

- ✅ Fine-tuned **Stable Diffusion XL** using **DreamBooth + LoRA**
- 💾 Used `diffusers`, `peft`, `transformers`, and `accelerate`
- 🖼️ Trained on 1024×1024 resolution, batch size 1
- ⚙️ GPU: NVIDIA L4 (24GB) via Google Colab Pro
- 🧠 Enabled xFormers and fp16 mixed precision
- 📝 Captions embedded as a tab-separated file (`captions.txt`)

---

## 📈 Evaluation & Results

### Best Fine-Tuned Results:
| Metric         | Score     |
|----------------|-----------|
| CLIP Score     | 0.3558    |
| ITI Similarity | 0.2368    |

- Achieved strong **zero-shot generalization** on novel, hybrid prompts
- Outperformed all baseline models in alignment and visual storytelling
- Human evaluators preferred fine-tuned outputs even when scores were moderate

---

## 💬 Example Zero-Shot Prompt

> "A cheerful green dragon flying over a magical forest with a wizard and a princess waving from below."

<img width="827" height="833" alt="image" src="https://github.com/user-attachments/assets/449d1a65-6b5f-40ae-8383-27e8d27de25c" />


---

## ⚠️ Challenges

- Prompt sensitivity and stochastic generation
- Visual artifacts in complex scenes
- Character blending (e.g., wizard and princess features)
- Discrepancy between human preferences and metric scores

---

## 🔮 Future Work

- Expand dataset with diverse characters and themes  
- Add safety features (RLHF, NSFW filters, watermarking)  
- Integrate with interactive storytelling apps or web demos  
- Improve character consistency and facial rendering

---
