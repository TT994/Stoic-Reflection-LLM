# Stoic Reflection LLM – Marcus Aurelius Persona Fine-Tuning

This repository contains the code, dataset, and LoRA adapters for **MABot**, a Stoic-inspired
reflection companion fine-tuned on *Phi-3 Mini (4k Instruct)*.  
The goal is to explore how generative models can support **affective human–AI interaction**
without recreating a real individual or generating high-risk identity illusions.

This project was developed as part of the Cognitive Science & Artificial Intelligence
course on **Generative AI and Affective Computing**.

---

## 🧠 Overview

MABot is a **text-based, non-embodied chatbot** trained to emulate the reflective,
philosophical tone of *Marcus Aurelius’ Meditations*.  
It aims to provide calm and structured emotional reframing while avoiding the ethical risks
associated with griefbots or identity-simulation systems.

The project demonstrates:

- Persona transfer through LoRA fine-tuning  
- Emotional reasoning aligned with Stoic philosophy  
- Successful responses in affect-sensitive prompts  
- Failure cases involving identity hallucination  
- Ethical analysis inspired by digital-afterlife literature

---

## 🚀 Model

**Base Model:** `microsoft/Phi-3-mini-4k-instruct`  
**Fine-Tuning Method:** LoRA (Low-Rank Adaptation)  
**Frameworks:** Hugging Face Transformers, PEFT, PyTorch  
**Compute:** Google Colab T4 GPU

**Why Phi-3 Mini?**
- Lightweight (3.8B parameters)
- Instruction-tuned
- Runs reliably on Colab
- Strong reasoning performance for its size

**Why LoRA (not QLoRA)?**
- QLoRA caused CUDA/triton errors on Colab
- LoRA FP16 was stable and memory-efficient
- Perfect for small models like Phi-3 Mini

---

## 📘 Dataset

The dataset consists of ~216 instruction–response pairs representing Stoic guidance about:

- Anger  
- Grief  
- Uncertainty & fear  
- Emotional control  
- Virtue & judgment  
- Acceptance and impermanence  

All responses are original paraphrases written in the *style* of Marcus Aurelius.
No copyrighted material or real-person identity reconstruction is used.

---

## 🔧 Fine-Tuning

LoRA hyperparameters:

---

## 📘 Dataset

The dataset consists of ~216 instruction–response pairs representing Stoic guidance about:

- Anger  
- Grief  
- Uncertainty & fear  
- Emotional control  
- Virtue & judgment  
- Acceptance and impermanence  

All responses are original paraphrases written in the *style* of Marcus Aurelius.
No copyrighted material or real-person identity reconstruction is used.

---

## 🔧 Fine-Tuning

LoRA hyperparameters:


---

## 📘 Dataset

The dataset consists of ~216 instruction–response pairs representing Stoic guidance about:

- Anger  
- Grief  
- Uncertainty & fear  
- Emotional control  
- Virtue & judgment  
- Acceptance and impermanence  

All responses are original paraphrases written in the *style* of Marcus Aurelius.
No copyrighted material or real-person identity reconstruction is used.

---

## 🔧 Fine-Tuning

LoRA hyperparameters:

r = 16
lora_alpha = 32
lora_dropout = 0.05
target_modules = ["q_proj", "k_proj", "v_proj", "o_proj"]
batch_size = 2
grad_accumulation = 8
learning_rate = 2e-4
epochs = 2


## 📂 Repository Structure

