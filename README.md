# Importance of pre-tokenization in multi-tier LLMS

![Python 3.9+](https://img.shields.io/badge/Python-3.9+-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Frameworks](https://img.shields.io/badge/Frameworks-PyTorch%2C%20Transformers-orange.svg)

This repository contains the source code, data, and analysis for the undergraduate thesis project focused on the computational efficiency of Large Language Models (LLMs), specifically addressing the impact of pre-tokenization strategies on morphologically rich languages like Portuguese compared to English.

## Abstract

The efficiency of Large Language Models (LLMs) is critically dependent on the pre-tokenization stage, which lacks a systematic approach, especially for morphologically rich languages like Portuguese. This work addresses this gap through an empirical investigation with a strong software engineering focus. A software prototype was developed and validated to comparatively analyze the impact of pre-tokenization strategies on the computational efficiency of multilingual (XLM-R, mT5) and generative (Gemma) LLMs in Portuguese and English. The results confirmed the central hypothesis: Portuguese exhibited a less efficient tokenization, with a fertility rate (tokens per word) approximately 9.5% higher than English on the mT5 model. This project provides concrete evidence of this "efficiency tax" and offers a reproducible blueprint for analyzing and optimizing NLP pipelines.

## Key Features

- **Comparative Analysis:** Quantitatively measures the tokenization efficiency disparity between Portuguese and English.
- **Modular Prototype:** A reusable Python pipeline to test different pre-processing strategies.
- **Reproducible Results:** All scripts, raw data, and generated figures are included to ensure full reproducibility.
- **Focus on Engineering Metrics:** Measures key indicators like token count, fertility (tokens/word), and inference latency.

## Repository Structure

tcc-eficiencia-tokenizacao/

├── notebook/  
├── results/  
├── figures/  
├── README.md  
├── LICENSE  
├── .gitignore  
└── requirements.txt

## 🚀 Setup and Installation

To replicate the environment and run the experiments, please follow these steps. A GPU is required for the dynamic analysis part of the experiment.

**1. Clone the repository:**

```bash
git clone [https://github.com/your-user/your-repository.git](https://github.com/your-user/your-repository.git)
cd your-repository
```

```bash
# Recommended -  Create and activate a virtual environment:
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

```bash
# Install the required dependencies:
pip install -r requirements.txt
```

## How to Run the Experiment

All the code for data collection, analysis, and visualization is contained within a single Jupyter Notebook.

- Navigate to the notebook/ directory.
- Open and run the cells in experiment.ipynb using Jupyter Lab or Google Colab.
- The notebook is self-contained and will:
- Download the necessary datasets and models from the Hugging Face Hub.
- Run the pre-processing strategies.
- Collect static and dynamic metrics.
- Save the results to a CSV file (a copy is already in the resultados/ folder).
- Generate the analysis plots.

## Results

The core finding confirms that standard multilingual models tokenize Portuguese less efficiently than English. For instance, with the google/mt5-base tokenizer, Portuguese texts required ~9.5% more tokens per word on average.

The complete set of raw results is available in resultados/experiment_results.csv. The detailed discussion and interpretation of these results can be found in the full thesis document.

## How to Cite

If you use this code or our findings in your research, please cite this work.

```Snippet de código
@mastersthesis{Elvas2025,
  author  = {Joao Elvas},
  title   = {Análise Empírica do Impacto de Estratégias de Pré-Tokenização na Eficiência Computacional de Modelos de Linguagem},
  school  = {Universidade de Brasília (UnB), Faculdade do Gama (FGA)},
  year    = {2025},
  address = {Gama, DF},
  url     = {https://github.com/joao-elvas/TCC1}
}
(Note: Please adjust the BibTeX key and details as you see fit.)
```

## License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
