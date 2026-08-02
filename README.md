# MNIST CNN Classifier

A compact convolutional neural network for classifying handwritten digits from the MNIST dataset. The notebook focuses on a clean, reproducible CNN workflow and includes saved training and evaluation outputs.

## Dataset

The repository includes `data/mnist.pkl.gz`, containing 60,000 training images and 10,000 test images. Each example is a 28×28 grayscale image labeled from 0 to 9.

## Approach

The notebook scales pixel values, creates a validation split from the training data, and trains a small two-block CNN with dropout. It evaluates the final model with test accuracy, a per-class report, a confusion matrix, and examples of misclassified digits.

To keep the project practical on CPU, training uses a seeded 20,000-image subset while evaluation uses the full test set.

## Run

1. Create a Python environment.
2. Install dependencies with `pip install -r requirements.txt`.
3. Open `cnn-mnist-classifier.ipynb` from the repository root.
4. Run all cells in order.

## Result

The final clean run reached **98.09% test accuracy** with a test loss of **0.0578**. The compact model reaches this result despite using only part of the available training set.

## Limitations

- The model is intentionally small and not exhaustively tuned.
- Training uses a subset of MNIST for bounded CPU runtime.
- MNIST is cleaner and more centered than real-world handwriting images.
