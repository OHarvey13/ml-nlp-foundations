# ML + NLP Foundations
Building intuition in text representation, classic ML models, and neural networks as a foundation for LLMs.

This repo is the first step in my **LLM Deep Dive** journey.
It covers:

- Phase 1: Classic ML for text (Bag-of-Words, TF-IDF, Naive Bayes, Logistic Regression)
- Phase 2: Neural networks for text (RNNs, LSTMs, embeddings)

Goal: understand text representation, model limitations, and lay groundwork for neural networks and LLMs.

ml-nlp-foundations/  
│── phase1_text_classification/   # Classic ML experiments    
│   ├── notebooks/   
│   ├── data/   
│   └── README.md   
│    
│── phase2_neural_nets/           # Neural networks experiments  
│   ├── notebooks/  
│   ├── data/  
│   └── README.md  
│  
│── shared_utils/                 # Tokenizers, helper functions   
│  
├── requirements.txt  
└── README.md                     # This overview  

# Requirements
- Python >= 3.10
- Jupyter Notebook
- scikit-learn
- numpy, pandas
- matplotlib / seaborn (optional for visualization)

# Quick start
1. Clone the repo
2. Install requirements: `pip install -r requirements.txt`
3. Explore Phase 1 notebooks: `phase1_text_classification/notebooks/01_text_classification.ipynb`

- Each phase has its own folder with notebooks and datasets
- Notebooks mix code, outputs, and reflection prompts
- Fill in answers to the questions in the README or notebook Markdown
- Phase 2 builds on Phase 1, introducing neural networks for text

- Phase 1: Key learnings and limitations of BoW / TF-IDF
- Phase 2: Insights from RNNs and embeddings
- Observations that prepare me for LLM experiments
