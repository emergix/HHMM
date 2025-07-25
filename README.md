# Learning Transition in Hierarchical Hidden Markov Models

This repository presents a theoretical framework for learning transitions in **Hierarchical Hidden Markov Models (HHMMs)** using **probabilistic graphical models** and **tensor-based inference**. The approach builds upon classical EM algorithms and introduces a recursive, modular, and scalable methodology for learning latent variable structures.

📄 **Read the paper**: [LearningTransition.pdf (francais)](./Docs/LearningTransition.pdf)

📄 **Read the paper**: [LearningTransition.pdf (Conclusion : English)](./Docs/LearningTransition_EN.pdf)

---

## 📘 Overview

This work offers a deep exploration of learning structured probabilistic models, especially in settings where latent hierarchical relationships exist and must be inferred from limited data. The key ideas include:

- Probabilistic interpretation of expert systems and inference rules
- Reformulation of EM learning via free energy minimization
- Tensor-based formulation of transition probabilities
- Scalable construction of HHMMs with correlation modeling
- Generalization to infinite hierarchical depth with abstraction levels

---

## 🧠 Core Contributions

### 1. Probabilistic Graphical Models
A reinterpretation of expert systems using **Bayesian networks**, where inference is driven by **likelihood optimization** rather than heuristic rules.

### 2. EM Algorithm and Variational Formulation
The **E-step** of EM is presented as an expectation over hidden transition structures, leading to:
- Lagrangian optimization
- Free energy formulations
- Legendre duality in parameter space

### 3. Tensorial Representation of Transitions
Transition rules are embedded in **tensor spaces**:
- Sufficient statistics computed via marginalizations
- Recursive structure over time slices
- Matrix products replaced by **tensor contractions**

### 4. Hierarchical HMMs with Correlations
Extensions of HMMs to:
- Multiple hidden layers
- Intermediate latent variables capturing **correlations**
- Modular inference over composite structures

### 5. Infinite Hierarchy and Activation Variables
Introduction of a hidden **abstraction index** \( n \in \mathbb{N} \) with:
- Decaying priors to enforce sparsity
- Recursive initialization and transition rules
- Flattening to an equivalent HMM by aggregation

---

## 📐 Mathematical Tools

- Lagrangian optimization under constraints
- Expectation-Maximization (EM)
- Legendre transforms and duality
- Tensor algebra and contraction
- Conditional Data Log-Likelihood (CDLL)

---

## 🔍 Use Cases

- Time-series modeling with deep latent structure
- Natural language processing with hierarchical syntax
- Bioinformatics or signal processing with hidden states
- Learning structured priors in small data regimes

---

## 📎 File Structure

