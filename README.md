# LLM Benchmarking and Model Selection Framework

## Overview

Selecting the right Large Language Model (LLM) for a specific application requires balancing multiple factors such as response quality, inference speed, model size, and computational efficiency.

This project presents a systematic framework for evaluating and ranking pre-trained text generation models using the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) multi-criteria decision-making algorithm.

The framework benchmarks multiple transformer-based language models on real-world text generation tasks and identifies the most suitable model based on configurable evaluation criteria.

---

## Features

* Evaluate multiple pre-trained text generation models
* Measure real inference latency
* Compare model sizes
* Estimate language generation quality
* Calculate perplexity scores
* Rank models using TOPSIS
* Generate visual performance comparisons
* Support customizable evaluation weights

---

## Models Evaluated

| Model       | Architecture                               |
| ----------- | ------------------------------------------ |
| GPT-2       | Decoder-only Transformer                   |
| DistilGPT-2 | Distilled GPT-2                            |
| T5-Small    | Encoder-Decoder Transformer                |
| BART-Base   | Denoising Sequence-to-Sequence Transformer |

---

## Evaluation Metrics

The framework evaluates models using four key criteria:

| Metric             | Description                    | Type    |
| ------------------ | ------------------------------ | ------- |
| Generation Quality | Richness of generated output   | Benefit |
| Inference Latency  | Time required to generate text | Cost    |
| Model Size         | Memory footprint of the model  | Cost    |
| Perplexity         | Language modeling confidence   | Cost    |

---

## Methodology

The project implements TOPSIS from scratch without relying on external decision-making libraries.

### Workflow

1. Load pre-trained language models
2. Generate outputs using a common prompt
3. Extract evaluation metrics
4. Construct decision matrix
5. Normalize metrics
6. Apply weighted scoring
7. Compute ideal best and worst solutions
8. Calculate Euclidean distances
9. Generate TOPSIS scores
10. Rank models by closeness coefficient

---

## System Architecture

```text
Input Prompt
      │
      ▼
Pre-trained LLMs
(GPT-2, DistilGPT-2, T5, BART)
      │
      ▼
Performance Evaluation
      │
      ├── Generation Quality
      ├── Latency
      ├── Model Size
      └── Perplexity
      │
      ▼
Decision Matrix
      │
      ▼
TOPSIS Algorithm
      │
      ▼
Model Ranking
      │
      ▼
Visualization Dashboard
```

---

## Tech Stack

* Python
* Hugging Face Transformers
* PyTorch
* NumPy
* Pandas
* Matplotlib

---

## Installation

```bash
git clone https://github.com/sukhijashivam/Text_Generation_Topsis.git

cd Text_Generation_Topsis

pip install -r requirements.txt
```

---

## Run

```bash
python main.py
```

---

## Results

The framework produces:

* Performance comparison tables
* TOPSIS scores
* Model rankings
* Visualization charts

The model with the highest TOPSIS score is identified as the optimal text generation model under the selected evaluation criteria.

---

## Applications

* LLM Selection
* AI Product Development
* NLP Research
* Model Benchmarking
* Resource-Constrained Deployments
* Generative AI Systems

---

## Future Improvements

* Support for Llama Models
* Support for Mistral Models
* RAG-based evaluation
* Human preference scoring
* Automated prompt benchmarking
* Multi-dataset evaluation

---

## Author

Shivam Sukhija

Computer Engineering, Thapar Institute of Engineering and Technology

Focused on Machine Learning, Generative AI, and Backend Development.

