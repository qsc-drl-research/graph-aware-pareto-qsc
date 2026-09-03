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
