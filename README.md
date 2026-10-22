# GPU Optimisation of an Image Classification Pipeline with TensorFlow and Keras

## Project Overview

This project investigates GPU-aware optimisation techniques for an image classification pipeline built with TensorFlow and Keras. Using the CIFAR-10 dataset, it compares a baseline convolutional neural network (CNN) with an optimised implementation.

The work focuses on improving the data input pipeline and model training performance while evaluating classification accuracy and loss.

## Objectives

- Develop and evaluate a baseline CNN for CIFAR-10 image classification.
- Optimise data loading and preprocessing.
- Apply caching, parallel mapping and prefetching to the data pipeline.
- Improve the model architecture using batch normalisation and dropout.
- Compare baseline and optimised training and validation performance.
- Evaluate classification errors using prediction examples and a confusion matrix.

## Dataset

**CIFAR-10** is an image classification dataset containing images from 10 classes:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

The images are RGB images with a resolution of 32 × 32 pixels. The notebook loads CIFAR-10 using TensorFlow Datasets (`tensorflow_datasets`).

## Technologies Used

- Python
- TensorFlow
- Keras
- TensorFlow Datasets
- NumPy
- Matplotlib
- Google Colab or a compatible Jupyter environment

## Methodology

### 1. Baseline CNN

A convolutional neural network is trained on CIFAR-10 to establish baseline classification performance. Training and validation loss and accuracy are monitored across epochs.

### 2. Data Pipeline Optimisation

The optimised pipeline uses:

- **Caching** to reduce repeated data-loading work.
- **Parallel mapping** to improve preprocessing throughput.
- **Prefetching** to overlap data preparation and model execution.

These techniques aim to reduce input pipeline bottlenecks and improve hardware utilisation.

### 3. Model Optimisation

Batch normalisation and dropout are incorporated into the CNN to support more stable training and help reduce overfitting.

### 4. Model Evaluation

Baseline and optimised models are evaluated using:

- Training and validation loss curves.
- Training and validation accuracy curves.
- Example image predictions.
- A confusion matrix to examine class-level classification errors.

## Reported Results

The accompanying report describes the following results:

| Metric | Baseline | Optimised |
|---|---:|---:|
| Validation accuracy | Approximately 71.8% | Approximately 79.2% |
| Validation loss | Approximately 0.91 | Approximately 0.63 |

These figures are taken from the accompanying report and should be checked against the final notebook outputs before being treated as definitive results.

The report also describes fewer differences between training and validation performance after optimisation, although the confusion matrix indicates that some classes remain harder to distinguish than others.

## Repository Structure

```text
gpu-optimisation-image-classification-tensorflow/
├── README.md
├── Keras_Assignment_GPU_Optimisation_in_Tensorflow_notebook_(Ref_Def_2025_2026)(5).ipynb
└── GPU Optimisation of an Image Classification Pipeline with TensorFlow and Keras (2).pdf
```

The notebook contains the implementation, while the PDF contains the written report and visual results.

## How to Run

1. Open the notebook in Google Colab or a compatible Jupyter environment.
2. Ensure TensorFlow, TensorFlow Datasets and other required dependencies are installed.
3. Run the notebook cells in order.
4. Review the baseline model, optimised pipeline and evaluation outputs.
5. Compare the final metrics and figures with the accompanying report.

A GPU-enabled runtime may be used where available. Actual training speed depends on the hardware, batch size, pipeline configuration and runtime environment.

## Limitations

- Results can vary with random initialisation, runtime hardware and training configuration.
- Validation accuracy alone does not fully describe performance across all classes.
- A confusion matrix is useful for identifying class-level errors, but further metrics may be needed for a complete evaluation.
- Performance claims should be supported by consistent measurements and, where possible, training-time comparisons between the baseline and optimised pipeline.

## Conclusion

This project compares a baseline CIFAR-10 CNN with an optimised TensorFlow and Keras implementation. It explores how data pipeline improvements and model regularisation techniques can affect image classification performance.

The reported results suggest improved validation accuracy and reduced validation loss after optimisation. The accompanying notebook and report provide the implementation, evaluation plots and discussion.

## Academic Context

Prepared for the GPU Optimisation of an Image Classification Pipeline with TensorFlow and Keras assignment. This repository documents the implementation and reported evaluation results for academic purposes.
