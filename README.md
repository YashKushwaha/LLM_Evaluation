# 🧪 LLM Evaluation Experiments

This project explores how to evaluate Large Language Models (LLMs) using a variety of question-answering and commonsense reasoning tasks. It's intended as a hands-on prototype to understand how different LLMs (e.g., **Mistral**, **Phi-4**, **LLaMA**) perform under specific test prompts and evaluation methods.

The code and notebooks demonstrate:
- Running LLMs on test cases
- Logging outputs to a MongoDB database
- Retrieving results for post-hoc evaluation
- Calculating metrics like **accuracy**, **exact match**, and potentially **LLM-as-a-judge** scoring

> ⚠️ **Note**: This is an exploratory, WIP (Work in Progress) project for learning and experimentation.

---

## 🗂️ Project Structure

```
yashkushwaha-llm_evaluation/
├── README.md                  # Project documentation
├── pyproject.toml             # Poetry config (optional use)
└── notebooks/
    ├── LLM runtime for QnA evaluation.ipynb
    ├── mistral evaluation.ipynb
    ├── Phi4 evaluation.ipynb
    ├── PIQA eval.ipynb
    ├── PIQA.ipynb
    └── [Exported .html versions of the above notebooks]
```

---

## 📌 Project Goals

- ⚙️ Test how different LLMs respond to structured input questions (e.g., QnA, PIQA)
- 🧾 Log generated answers to **MongoDB** for tracking and evaluation
- 📊 Evaluate outputs using metrics like:
  - Accuracy
  - Exact match (EM)
  - Optional: LLM-based scoring

---

## 🔧 Technologies Used

- **Jupyter Notebooks** for runtime and evaluation logic
- **Python** with Hugging Face or API-based LLM calls (assumed)
- **MongoDB** to persist model outputs
- **Poetry** for dependency management (optional)

---

## 🚀 How to Use

### 1. Run LLM Inference

Use the notebook:

```
notebooks/LLM runtime for QnA evaluation.ipynb
```

- Prompts are sent to the model (e.g., Mistral, Phi-4)
- Responses are saved to a MongoDB collection for later analysis

### 2. Evaluate Outputs

Run the evaluation notebooks, such as:

```
notebooks/mistral evaluation.ipynb
notebooks/Phi4 evaluation.ipynb
notebooks/PIQA eval.ipynb
```

- These load response data from MongoDB
- Compute metrics to assess model accuracy and behavior

---

## 🧠 Observations & Future Work

This is an evolving project. Possible enhancements include:

- Unifying runtime and evaluation via a shared library or script
- Adding support for multiple metrics (BLEU, ROUGE, BERTScore, etc.)
- Comparing zero-shot vs. few-shot performance
- Automating eval loops with LLM-as-a-judge methods

---

## 📚 References

- [OpenAI / Anthropic / Hugging Face APIs]
- [MongoDB Python Docs](https://pymongo.readthedocs.io/)
- [PIQA dataset](https://paperswithcode.com/dataset/piqa)
- [BoolQ dataset](https://paperswithcode.com/dataset/boolq)

---
