
# 🔁 Merged Mistral-LoRA for Resume Summarization & Entity Extraction

Welcome to the repo where we **merge and deploy two powerful LoRA models** on top of Mistral 7B for 🔹 resume summarization and 🔸 entity extraction.

This project includes:

- 🧠 Resume Summarizer: Generates a concise 2-line summary from resumes.
- 🏷️ Entity Extractor: Extracts key info like names, roles, companies, and education.
- 🔀 Merged Model: Combined into a single model using MergeKit with linear configuration.

> ✅ Final model hosted at: [Hugging Face – Impulse007/merged-mistral-lora2](https://huggingface.co/Impulse007/merged-mistral-lora2)

---

## 📂 Repository Contents

| File | Description |
|------|-------------|
| **`Mistralmerge.ipynb`** | 🔧 Contains the **merging code** using [MergeKit](https://github.com/arcee-ai/MergeKit). Merges `waelChafei/resume-summarization-finetuned-mistral-7b` and `Pennlaine/Mistral-7B-v02-Entity-Extraction` LoRAs on top of Mistral-7B. Also includes code to **upload the final model to Hugging Face**. |
| **`Results.ipynb`** | 🧪 Runs and tests **each LoRA model individually**, and then **loads the final merged model** from Hugging Face for combined testing. Allows testing from the command line using simple text prompts. |
| **`linear.yml`** | ⚙️ MergeKit **linear merge configuration** file, which controls how the weights of both LoRAs are combined in the final model. |

---

## 🔐 Hugging Face Token Setup

In order to **upload or download private models** from Hugging Face, you’ll need to insert your personal token:
### from huggingface_hub import login 
### login("your-hugging-face-access-token")

## ✨ How to Use the Merged Model
You can interact with the merged model in the terminal using prompts like:

Summarize: John has 5 years of experience in AI at Google and Tesla.
Extract entities: Sarah worked at IBM in NLP and has an MS from Stanford.
Summarize and extract entities: Michael worked at OpenAI and studied CS at MIT.
