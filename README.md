# Evaluating_LLM
# **LLM Evaluation on Question Answering Datasets**

## 📋 **Overview**
This repository contains the evaluation of **Large Language Models (LLMs)** for **Question Answering (QA)** tasks using two datasets:
1. **Stanford Question Answering Dataset (SQuAD)** - A widely-used English reading comprehension dataset. [SQuAD](https://huggingface.co/datasets/rajpurkar/squad)
2. **Custom Arabic QA Dataset** - Created by web scraping Arabic Wikipedia articles and generating questions and answers using **ChatGPT-4**.

### **Objective**
To evaluate the performance of various LLMs in generating accurate and faithful answers to questions based on given contexts. The evaluation includes:
- Automatic metrics like **ROUGE** and **BLEU**.
- LLM-as-a-Judge evaluation for **relevance**, **faithfulness**, **bias**, and **toxicity**.

---

## 📁 **Repository Structure**
```plaintext
├── Data/  
│   ├── squad_dataset.csv          # SQuAD dataset
│   └── arabic_dataset.csv         # Custom Arabic dataset
├── LLMs_Evaluation/  
│   ├── Gpt_4o_mini_VS_Naseej_noon_7b_VS_Omartificial_intelligence.ipynb 
│   └── google-gemma-vs-hesham-llm.ipynb      
├── LLMs_Generated_Answers/  # Holding generated answers for 5 models
├── Relevance & Faithfullness/  # Tested Relevance & Faithfullness on old versions of data
├── Results/  
│   ├── results.odt          # Summary of evaluation results
│   └── Hesham_Gemma_Quick_Report.docx    # Quick notes 
├── LICENSE                        # Project license
├── README.md                      # Documentation (this file)
└── data-generation.ipynb          # Arabic dataset generation notebook
```

---

## 🔍 **Models Evaluated**
The following LLMs were tested:
1. **GPT-4o-mini**  
2. [**google/gemma-2-2b**](https://huggingface.co/google/gemma-2-2b)
3. [**HeshamHaroon/Arabic-llama3**](https://huggingface.co/HeshamHaroon/Arabic-llama3/tree/main)
4. [**Naseej/noon-7b**](https://huggingface.co/Naseej/noon-7b)
5. [**Omartificial-Intelligence-Space/Arabic-llama3.1-16bit-FT**](https://huggingface.co/Omartificial-Intelligence-Space/Arabic-llama3.1-16bit-FT)

---

## 📊 **Datasets**
### **1. SQuAD Dataset**
- A widely-used English reading comprehension dataset.
- Questions are based on Wikipedia articles, with answers either being spans of text or marked as "unanswerable."

### **2. Custom Arabic Dataset**
- Scraped from Arabic Wikipedia articles.
- **ChatGPT-4** was used to generate questions and answers based on the scraped contexts.
- The data was reviewed, cleaned, and adjusted to include varying token sizes for input contexts.

#### Notes on the Arabic Data 
Description:
Articles were scraped from Arabic Wikipedia.
GPT-4 was used to generate questions and answers based on the scraped context.
The dataset was manually reviewed for:
Cleaning answers.
Editing contexts to vary the token sizes (to ensure models handle different input lengths).
The dataset contains Arabic contexts and corresponding questions.

Purpose:
To evaluate models on Arabic text comprehension and answer generation.

Dataset Characteristics:
Diverse context lengths: Token sizes are not fixed but vary, testing the models' ability to handle inputs of different lengths.
Manual cleaning and review: The data was refined for accuracy and relevance.

---

## ⚙️ **Setup Instructions**

### **1. Prerequisites**
Ensure you have the following tools installed:
- **Python**: >= 3.9
- **PyTorch**: >= 2.0
- **HuggingFace Transformers**
- [**MLflow**](https://mlflow.org/docs/latest/llms/rag/notebooks/question-generation-retrieval-evaluation.html): For question and answer generation

## 📈 **Evaluation Metrics**
### **1. Automatic Metrics**
- **ROUGE-1**, **ROUGE-2**, **ROUGE-L**
- **BLEU**

### **2. LLM-as-a-Judge**
[LLM-as-a-Judge_Hugging Face](https://huggingface.co/learn/cookbook/llm_judge)
- **Relevance**: How well the answer matches the question.
- **Faithfulness**: Ratio of claims in the answer that match the context.
- **Bias**: Analysis of biases in the answers.
- **Toxicity**: Detection of harmful or inappropriate content.

---

## 📄 **Findings**
The evaluation revealed strengths and weaknesses in each LLM's ability to generate accurate, faithful, and unbiased answers. Detailed results can be found in the **Results/** folder.

---
**Authors**
- Aya Khaled
- Yara Ramadan Zidan
- For questions or contributions, please contact [yukikhaled@gmail.com], [yarazedan980@gmail.com].

---

## 📜 **License**
This project is licensed under the **MIT License**. See the LICENSE file for details.

---
