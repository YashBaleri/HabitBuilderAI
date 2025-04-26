# HabitBuilder AI 🧐✨

**Memory-Efficient Fine-Tuning and Deployment of Habit-Building AI**

---

## 🔬 Project Background

This project was originally developed for the graduate course **Applied Machine Learning**. The objective was to explore and implement **efficient fine-tuning techniques for large language models (LLMs)**, focusing on overcoming VRAM limitations without sacrificing model quality.

HabitBuilder AI fine-tunes large models like **Llama2-7B** and **Mistral-7B** using **QLoRA** and **4-bit quantization**, adapting them to provide **habit-building advice** inspired by James Clear's "Atomic Habits." The final model is deployed through **Replicate API** for real-time inference.

While we’ve implemented **Retrieval-Augmented Generation (RAG)** for context-aware responses based on a single dataset (\"Atomic Habits\"), we plan to expand this system in the future to include a **broader range of books** and data sources to make the assistant more robust and versatile.

---

## 🚀 Project Overview

HabitBuilder AI demonstrates how to fine-tune large-scale language models efficiently on resource-constrained environments (like Google Colab T4 GPUs), adapting them to custom domains, and deploying them as lightweight AI assistants.

---

## ✨ Key Features

- Fine-tunes Llama2 and Mistral 7B models with **QLoRA** for low-VRAM usage
- Applies **4-bit quantization** using **BitsAndBytes** for memory efficiency
- Trains models using **parameter-efficient fine-tuning (PEFT)** with LoRA adapters
- Custom dataset creation from **"Atomic Habits"** for domain-specific knowledge
- Real-time deployment using **Replicate API**
- Simple prompt-based interface for advice generation
- Implemented **Retrieval-Augmented Generation (RAG)** for context-aware habit-building insights

---

## 🛠️ Technologies Used

- **Python**
- **Hugging Face Transformers**
- **PEFT (QLoRA/LoRA)**
- **BitsAndBytes**
- **Accelerate**
- **TRL (Trainer Library)**
- **PyTorch**
- **Replicate API**

---

## 🏢 Architecture Overview

```
Custom Dataset (Guanaco/Atomic Habits)
        ⬇
QLoRA Fine-Tuning on Llama2/Mistral7B
        ⬇
4-bit Quantization with BitsAndBytes
        ⬇
Merging LoRA Adapters
        ⬇
Real-Time Inference via Replicate API
```

---

## 🔹 File Descriptions

- **README.md**:

  > This guide. Provides an overview of the project, goals, features, architecture, and instructions.

- **Fine_Tune_Llama2.ipynb**:

  > Fine-tunes the **Llama2-7B** model on the **Guanaco dataset** using QLoRA, 4-bit quantization, and Hugging Face's `SFTTrainer`.

- **QLora.ipynb**:

  > Fine-tunes the **Mistral-7B** model on a custom dataset derived from **"Atomic Habits"**, formatting it into **ChatML style** for conversational AI use-cases.

- **HabitBuilderAI.ipynb**:
  > Deploys the fine-tuned model through the **Replicate API**; defines a simple Python function to submit prompts and retrieve real-time habit-building advice.

---

## ⚙️ How to Run

> **Note**: Requires access to Google Colab and a Replicate API token.

1. Clone the repository:

```bash
git clone https://github.com/yourusername/HabitBuilderAI.git
```

2. Install required dependencies:

```bash
pip install -r requirements.txt
```

3. Fine-tune the models:

   - For Llama2: Run `Fine_Tune_Llama2.ipynb`
   - For Mistral7B: Run `QLora.ipynb`

4. Deploy for real-time inference:
   - Run `HabitBuilderAI.ipynb` and provide your Replicate API token.

---

## 🔮 Future Work

- Expand datasets beyond "Atomic Habits" for broader self-improvement advice.
- Build a **full-stack chatbot UI** using React or Next.js for public deployment.

---

## 🙏 Acknowledgements

- Hugging Face Ecosystem
- BitsAndBytes Library Developers
- Open Source contributors for Llama2, Mistral 7B, and QLoRA research

---

## 🔺 TL;DR

> Fine-tuned large LLMs on constrained hardware for domain-specific habit-building advice and deployed real-time AI assistants through Replicate API.
