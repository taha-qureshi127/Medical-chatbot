# 🩺 AI Medical Reasoning Chatbot

This repository contains a specialized medical reasoning chatbot fine-tuned on the DeepSeek-R1-Distill-Llama-8B model. It leverages Chain-of-Thought (CoT) reasoning to process clinical symptoms step-by-step before providing a highly accurate diagnosis.

## Features
* **Chain-of-Thought Logic:** Transparent `<think>` tags display the model's internal diagnostic process.
* **Parameter-Efficient Fine-Tuning:** Trained using LoRA and 4-bit quantization via Unsloth for extreme memory efficiency.
* **Local Deployment:** Configured out-of-the-box as a medical chatbot application hosted locally on port 8501.

## Tools & Technologies
* **Base Model:** DeepSeek-R1-Distill-Llama-8B
* **Frameworks:** Unsloth, Hugging Face (`transformers`, `trl`, `datasets`), PyTorch
* **Dataset:** FreedomIntelligence/medical-o1-reasoning-SFT

## Setup and Installation

1. **Clone the repository:**
   ```bash
   git clone (https://github.com/taha-qureshi127/Medical-chatbot)
   cd Medical-Chatbot
Install the dependencies:

pip install unsloth transformers trl datasets torch 

Usage
Running the Interface
Start the web interface to interact with the AI. This will start the medical chatbot application hosted locally on port 8501:

python app.py

Terminal Testing
To run a quick diagnostic test directly from the terminal without starting the full application:


python test_inference.py
Example Output
Input:

"A 61-year-old woman complains of involuntary urine loss when coughing or sneezing. What is the most likely diagnosis?"

AI Response:

<think>
The patient is a 61-year-old woman experiencing urine loss during activities that increase intra-abdominal pressure (coughing, sneezing). This presentation is classic for stress urinary incontinence, which is often caused by urethral hypermobility or intrinsic sphincter deficiency...
</think>

The most likely diagnosis is Stress Urinary Incontinence.
