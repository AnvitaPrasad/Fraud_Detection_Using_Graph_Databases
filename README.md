![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)

# Fraud Detection Using Graph Databases & Machine Learning

**F**raud **P**rediction using **G**raph features and machine learning techniques.

This project combines graph database techniques with machine learning to detect fraudulent transactions in financial payment systems. By leveraging graph-based features and advanced sampling methods, the system achieves improved fraud detection accuracy on highly imbalanced datasets.

Evaluations and results are summarized in the directory [evaluations](https://github.com/AnvitaPrasad/Fraud_Detection_Using_Graph_Databases/blob/main/fpg/evaluations/evaluations.md)

## Dataset

1. We use a dataset available on Kaggle - [Synthetic data from a Financial payment system](https://www.kaggle.com/ntnu-testimon/banksim1).
2. All raw data is stored in the [data](https://github.com/AnvitaPrasad/Fraud_Detection_Using_Graph_Databases/tree/main/fpg/data) directory.

## Software Dependencies

- Python 3.6+
- Required packages are listed in `fpg/requirements.txt`

### Installation

```bash
pip install -r fpg/requirements.txt
```

## Steps to Execute Code

### 1. Jupyter Notebooks
Navigate to the notebooks directory and launch Jupyter:
```bash
cd fpg/code/notebooks
jupyter notebook
```
From the Jupyter web interface, you can open and run any of the available notebooks.

### 2. Self-Paced Sampling Example
Execute the self-paced ensemble sampling:
```bash
cd fpg/code/sampling
python3 using_self_paced.py
```

### 3. Persona Graph Embeddings
Run the persona graph embedding algorithm:
```bash
cd fpg/code/persona
python3 -m graph_embedding.persona.persona --input_graph=${graph} --output_clustering=${clustering_output}
```

#### References

1. _Bryan Perozzi, Rami Al-Rfou, Steven Skiena_. DeepWalk: Online Learning of Social Representations 2018

2. _Epasto, Alessandro, and Bryan Perozzi_. "Is a single embedding enough? learning node representations that capture multiple social contexts." In The World Wide Web Conference, pp. 394-404. 2019.

3. _Zhining Liu, Wei Cao, Zhifeng Gao, Jiang Bian, Hechang Chen, Yi Chang, Tie-Yan Liu_. Self-paced Ensemble for Highly Imbalanced Massive Data Classification.  September 2019

4. _Brownlee, Jason_. SMOTE Oversampling for Imbalanced Classification with Python - https://machinelearningmastery.com. January 2017

5. "Finding Needles in a Haystack With Graph Databases and Machine Learning" - DZone AI

6. "Learn How to Perform Feature Extraction from Graphs using DeepWalk" - Analytics Vidhya

## Key Features

- **Graph-based Feature Extraction**: Utilizes DeepWalk and Persona algorithms for learning node representations from transaction graphs
- **Advanced Sampling Techniques**: Implements self-paced ensemble methods to handle highly imbalanced fraud datasets
- **Multiple Clustering Approaches**: Includes K-Means, DBSCAN, OPTICS, Agglomerative, and Birch clustering algorithms
- **Comprehensive Evaluation**: Detailed performance metrics and visualizations

## Project Structure

```
fpg/
├── code/
│   ├── notebooks/       # Jupyter notebooks for analysis and modeling
│   ├── persona/         # Graph embedding implementations
│   └── sampling/        # Self-paced ensemble sampling
├── data/               # Raw transaction data
└── evaluations/        # Results and evaluation metrics
```

## Author

**Anvita Prasad**

Original implementation based on research project CSE 573 Spring 2020 Group 12
