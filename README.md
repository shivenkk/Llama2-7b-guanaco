# Fine-Tuned Llama-2 Chatbot

Efficient fine-tuning of Llama-2 7B model using QLoRA and supervised learning for conversational AI.

## 🤗 Model Available on HuggingFace
**[shivenkk/Llama-2-7b-chat-finetune](https://huggingface.co/shivenkk/Llama-2-7b-chat-finetune)**

## Overview
- **Base Model**: Llama-2 7B
- **Dataset**: Guanaco (10,000 conversation examples)
- **Method**: QLoRA (4-bit quantization) + PEFT
- **Hardware**: Trained on T4 GPU (16GB VRAM)

## Key Features
- Memory-efficient fine-tuning using 4-bit precision
- Parameter-Efficient Fine-Tuning (PEFT) for resource optimization
- Supervised Fine-Tuning (SFT) with TRL library

## Performance
- **BLEU Score**: 0.5-0.7 (context-dependent)
- Successfully deployed to HuggingFace Model Hub
- Optimized for limited computational resources

## Technologies
- PyTorch
- Hugging Face Transformers
- QLoRA (BitsAndBytes)
- PEFT
- TRL Library

## Usage
```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model_name = "shivenkk/Llama-2-7b-chat-finetune"
tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForCausalLM.from_pretrained(model_name)
```
