# LLM Evaluation and Model Selection Framework


This project evaluates multiple pre-trained text generation models using real performance metrics and ranks them using the TOPSIS multi-criteria decision-making approach.

---

## 🎯 Objective
The objective of this project is to select the most suitable pre-trained text generation model by:
- Testing models on a common input prompt
- Extracting real performance metrics
- Applying the TOPSIS methodology
- Ranking models based on closeness to the ideal solution

---

## 🤖 Models Evaluated
The following pre-trained text generation models were evaluated:

| Model Name     |
|---------------|
| GPT-2          |
| DistilGPT-2    |
| T5-Small       |
| BART-Base      |

All models were accessed using the **Hugging Face Transformers** library.

---

## 📊 Evaluation Criteria
Each model was evaluated using the following criteria:

| Criterion   | Description                                                     | Type     |
|------------|-----------------------------------------------------------------|----------|
| Quality     | Output length (word count) as a proxy for generation richness   | Benefit  |
| Latency     | Inference time required to generate text                        | Cost     |
| Model Size  | Size of the model in MB                                         | Cost     |
| Perplexity  | Measure of language modeling confidence                         | Cost     |

---

## ⚖️ Criteria Weights
The importance of each criterion was defined as follows:

| Criterion   | Weight |
|------------|--------|
| Quality     | 0.30   |
| Latency     | 0.25   |
| Model Size  | 0.20   |
| Perplexity  | 0.25   |

The sum of all weights equals **1**.

---

## 🧮 Methodology
The TOPSIS method was implemented from scratch without using any external TOPSIS libraries.  
The following steps were followed:

1. Construction of the decision matrix using extracted model metrics  
2. Normalization of the decision matrix using vector normalization  
3. Application of weights to the normalized matrix  
4. Identification of ideal best and ideal worst solutions  
5. Calculation of Euclidean distances from ideal solutions  
6. Computation of the closeness coefficient  
7. Ranking of models based on TOPSIS scores  

---

## 📈 Results
After applying TOPSIS, each model received a closeness coefficient score.  
The model with the **highest TOPSIS score** is considered the most suitable pre-trained model for text generation under the chosen criteria.

A bar graph was generated to visually compare the TOPSIS scores of all evaluated models.

---

## ▶️ How to Run the Project

### Install Dependencies
```bash
pip install torch transformers pandas numpy matplotlib sentencepiece
