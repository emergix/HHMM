# From HHMMs to Transformers: What We Learned from a Decade of Modeling Time Series with Context

*By Olivier Croissant*

---

📄 **Read the paper**: [LearningTransition.pdf (Conclusion : English)](./Docs/LearningTransition_EN.pdf)

## Introduction

Ten years ago, Hierarchical Hidden Markov Models (HHMMs) were the state of the art for learning abstract structure in time series. Today, although neural methods like Transformers dominate the landscape, HHMMs offer valuable lessons that can—and should—be revisited. In this post, we reflect on what HHMMs taught us, and how their ideas are resurfacing in modern architectures for contextual time series modeling.

## What HHMMs Got Right

- **Hierarchical Structure**: HHMMs modeled time as nested layers of abstraction, enabling coarse-to-fine interpretation of sequential data.
- **Compositional Reasoning**: The recursive transition logic of HHMMs made it possible to model repeated motifs or multi-scale dependencies.
- **Interpretable Latent States**: States in HHMMs had interpretable roles, often associated with semantic stages or context changes.

## What We Didn't Know Back Then

While powerful in theory, HHMMs were challenging in practice:

- **Learning was hard**: EM and message-passing scaled poorly to deep hierarchies.
- **Parametric rigidity**: Modeling assumptions often limited expressivity.
- **Data hunger**: Annotating hierarchical latent states proved unrealistic in many settings.

## Modern Tools That Make the Old Ideas Work

### From RNNs to Hierarchical Latent Models

RNNs (and later LSTMs) replaced latent states with continuous vectors and trained them end-to-end via gradient descent. But the abstraction levels seen in HHMMs were largely lost—until new latent-variable models (like Variational RNNs) reintroduced hierarchical reasoning with neural flexibility.

### Transformers Learn Structure (Even When We Don't Tell Them)

Transformers, built on self-attention, offer a fresh take:

- They learn long-range and hierarchical dependencies implicitly.
- Multi-head attention approximates factorized transitions.
- Stacking layers allows emergent abstraction—something HHMMs enforced explicitly.

### Neural State-Space Models and the Return of Structure

New models like neural SSMs and temporal VAEs revive structured modeling:

- **Latent dynamics are back**, but parameterized by deep networks.
- **Inference is amortized** using recognition networks.
- **Hierarchy can be learned** using nested latent variables.

## Lessons for the Future

The time series problems of today—finance, climate, user modeling—require:

- **Temporal abstraction**: Not all signals are at the same scale.
- **Context-awareness**: Predictions depend on latent regime or stage.
- **Interpretability**: Especially in high-stakes applications, understanding latent structure matters.

Modern deep learning lets us revisit HHMMs not as obsolete artifacts—but as blueprints for designing models that are structured, interpretable, and trainable at scale.

## Conclusion

We don’t have to choose between structure and learning. With the tools we have today—Transformers, variational inference, neural SSMs—we can build models that learn like HHMMs hoped to: modularly, hierarchically, and with context in mind.

