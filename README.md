# BoiCLIP Lite: Optimizing BioCLIP for Mobile Environments

**BoiCLIP Lite** aims to make BioCLIP, a powerful vision model for biological classification, suitable for mobile platforms. By reducing the size and computational demands of BioCLIP using knowledge distillation and transfer learning, this project enables mobile deployment. The mobile-optimized model will empower biologists to classify and discover species in real time, leveraging mobile sensors for field data collection and analysis.

---

## Data Sources

- **TreeOfLife-10M Dataset**: A large-scale dataset of over 10 million images covering more than 450,000 taxa. This dataset trains models to recognize fine-grained species distinctions and hierarchical relationships in the tree of life.

---

## Methods

### 1. Knowledge Distillation
- Train a smaller "student model" to mimic BioCLIP's hierarchical predictions using TreeOfLife-10M.
- Optimize the student model for mobile platforms through quantization and pruning.
- Evaluate the student model's performance in terms of accuracy, size, speed, and memory usage on mobile devices.

### 2. Mobile Implementation
- Convert the optimized model to TensorFlow.js format.
- Integrate with React Native's camera and UI components using the `tfjs-react-native` adapter.
- Publish a reusable npm package named **`react-bio-clip`**.

---

## Evaluation

### Model Performance
- Compare the student model's top-1 and top-5 accuracy to the original BioCLIP on the TreeOfLife-10M dataset.
- Evaluate the retention of hierarchical prediction capabilities.

### Mobile Device Performance
- Measure real-world performance, including:
  - Model size
  - Prediction latency at various image resolutions

---

## Readings

### CLIP Models
- [An Image is Worth 16x16 Words](https://arxiv.org/abs/2010.11929)
- [Learning Transferable Visual Models](https://arxiv.org/abs/2103.00020)
- [Reproducible Scaling Laws for Contrastive Learning](https://arxiv.org/abs/2212.07143)
- [BioCLIP: Vision Foundation Model for Tree of Life](https://arxiv.org/abs/2311.18803)

### Knowledge Distillation
- [Knowledge Distillation: A Survey](https://doi.org/10.1007/s11263-021-01453-z)
- [Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531)
- [Efficient Training with Distillation](https://arxiv.org/abs/2012.12877)

### Reducing Model Size and Latency
- [MobileNets: Efficient CNNs for Mobile](https://arxiv.org/abs/1704.04861)
- [TinyVIT: Small Vision Transformers](https://arxiv.org/abs/2207.10666)
- [MobileVIT: Mobile-Friendly Vision Transformers](https://arxiv.org/abs/2110.02178)

### Mobile Deployment
- [TensorFlow.js in React Native](https://www.tensorflow.org/js/tutorials/applications/react_native)

---

## Goals
- Deliver an efficient BioCLIP Lite model for mobile platforms.
- Publish a reusable package to enable real-time biological classification in the field.
