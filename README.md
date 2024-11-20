# CIFAR-10 Image Classification with CNN: Sigmoid vs ReLU Activation

This project implements and compares two Convolutional Neural Networks (CNNs) for image classification on the CIFAR-10 dataset, exploring the impact of different activation functions (Sigmoid vs ReLU) on model performance.

## Overview

The project demonstrates:
- Implementation of CNNs using TensorFlow/Keras
- Comparison between Sigmoid and ReLU activation functions
- Data preprocessing and model evaluation
- Performance analysis on both standard and additional test sets

## Results

### Standard Test Set Performance
- Sigmoid Activation: 52.77% accuracy
- ReLU Activation: 67.23% accuracy

### Additional Test Set Performance
- Results vary based on the additional test data provided

## Model Architecture

Both models share the same architecture:
- 3 Convolutional layers
- 2 MaxPooling layers
- 2 Dense layers
- Output layer with 10 units (for CIFAR-10 classes)

The only difference is the activation functions used:
- Model 1: Sigmoid activation throughout
- Model 2: ReLU activation throughout

## Requirements

```
tensorflow
numpy
matplotlib
pickle
```

## Usage

1. Prepare your data directory structure:
```
data/
├── train/
│   ├── data_batch_1
│   ├── data_batch_2
│   └── data_batch_3
└── test/
    └── test_batch
```

2. Run the training script:
```python
python train.py
```

## File Structure

```
├── train.py         # Main training script
├── README.md        # This file
└── data/            # Data directory
```

## Key Findings

- ReLU activation significantly outperforms Sigmoid activation
- ReLU model shows ~15% better accuracy on the test set
- ReLU model converges faster during training

## Notes

- The models are trained for 10 epochs
- Adam optimizer is used for both models
- Images are normalized to [0,1] range
- SparseCategoricalCrossentropy is used as the loss function

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to open issues or submit pull requests for any improvements.
