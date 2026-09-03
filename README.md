# Graph-Aware State Representation and Pareto Dominance Filtering for Accelerated QoS-Aware Service Composition

This repository contains the implementation for the paper "Graph-Aware State Representation and Pareto Dominance Filtering for Accelerated QoS-Aware Service Composition."

## Overview
This project extends PPDRL, a pretraining-and-policy-based deep reinforcement learning framework for QoS-aware service composition, with two techniques:
1. **Graph-aware state representation** — eight DAG structural features added to the actor network's input.
2. **Pareto dominance filtering** — removes dominated candidate services per task before generating pretraining samples.

## Requirements
- Python 3.6.15
- TensorFlow 1.15.0

Install dependencies:
```bash
pip install -r requirements.txt
```

## Dataset
This project uses the QWS dataset (Al-Masri and Mahmoud, 2007), which contains 2,507 real web services classified into 233 categories. The dataset can be obtained from: https://dl.acm.org/doi/abs/10.1145/1242572.1242795.

The 233 service class groupings were generated using the text clustering method described in Liang et al. (2016), applied to the QWS dataset, following the same experimental setup as Yi et al.'s PPDRL framework. This clustering output is not redistributed here; users should generate it themselves by applying the clustering method to their own copy of the QWS dataset, or refer to the original PPDRL implementation.

## Usage
```bash
python main.py
```

## Repository Structure
- `main.py` — main entry point for training
- `actor.py` — actor network implementation
- `pareto_pruning.py` — Pareto dominance filtering module
- `sc_dataset.py` — dataset loading and batching
- `config.py` — configuration settings
- `optimizer.py`, `pretrain.py`, `generate.py` — supporting training components

## Citation
If you use this code, please cite:
