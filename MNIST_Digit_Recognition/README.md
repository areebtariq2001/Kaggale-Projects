# Handwritten Digit Recognition — Neural Network (Deep Learning)

## Overview
This project builds a Neural Network to recognize handwritten digits (0-9) from images, using the classic MNIST dataset. Unlike the other projects in this portfolio, this one introduces **Deep Learning concepts** — hidden layers, activation functions, and backpropagation — applied to image data.

## Dataset
**MNIST in CSV** — the "Hello World" dataset of computer vision, containing grayscale images of handwritten digits in an easy-to-use CSV format.

Source: [Kaggle — MNIST in CSV](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv)

- `mnist_train.csv` — 60,000 labeled training images
- `mnist_test.csv` — 10,000 labeled test images
- Each image is 28×28 pixels (784 pixel values), flattened into a single row, with a `label` column (0-9) indicating the digit.

## Project Workflow
1. **Data Loading & Inspection** — Loaded the pixel data and checked for missing values.
2. **Exploratory Data Analysis (EDA)** — Visualized the distribution of digit labels and displayed sample images by reshaping pixel rows back into 28×28 images.
3. **Preprocessing** — Normalized pixel values from the 0-255 range to 0-1, which helps the neural network train more effectively.
4. **Modeling** — Built a Neural Network using scikit-learn's `MLPClassifier` (Multi-Layer Perceptron) with two hidden layers (128 and 64 neurons) and ReLU activation.
5. **Evaluation** — Measured test accuracy, examined the confusion matrix, and reviewed precision/recall per digit class.
6. **Visualization** — Plotted the training loss curve and visually inspected correct vs. incorrect predictions on sample test images.

## Key Findings
- A simple Neural Network (no convolutional layers) achieves strong accuracy (~95-97%) on MNIST, showing how effective even basic deep learning architectures can be on well-structured image data.
- The confusion matrix typically reveals that visually similar digits (e.g., 4 and 9, or 3 and 8) are the most commonly confused pairs.
- This project used a fully-connected (Dense) network; a **Convolutional Neural Network (CNN)** would likely push accuracy even higher by better capturing spatial patterns in the images — a natural next step.

## Model Results
| Metric | Value |
|---|---|
| Test Accuracy | **[XX]%** *(replace with your Cell 10 output)* |

*(Optionally add a note on which digits were most often misclassified, based on your confusion matrix.)*

## Tech Stack
- Python
- Pandas, NumPy — data manipulation
- Matplotlib, Seaborn — visualization
- Scikit-learn — `MLPClassifier` neural network, evaluation metrics
- Joblib — model saving

## How to Run
1. Clone this repository.
2. Make sure `mnist_train.csv` and `mnist_test.csv` are in the same folder as the notebook.
3. Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn joblib`
4. Open `MNIST_Digit_Recognition.ipynb` in Jupyter Notebook and run all cells.

## Files
- `MNIST_Digit_Recognition.ipynb` — full analysis, training, and evaluation notebook
- `mnist_digit_model.pkl` — saved trained model
- `README.md` — project documentation
