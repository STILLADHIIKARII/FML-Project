
# Overparameterized CNN on MNIST — Weight Decay Experiment

This experiment demonstrates how L2 regularization (weight decay) affects overfitting behavior of the model, growth of model weight magnitudes
using a massively overparameterized CNN trained on a small subset of MNIST. This experiment also compares multiple weight decay values and visualizes impact of weight decay during training.


## Dataset
MNIST dataset which contains large number of handwritten digits and divided into training and testing set. Each image is a grayscale image of size 28x28 pixels.
The MNIST dataset contain 60k images for training set and uses other 10k images for testing set
## Training Setup
A small CNN is imployed containing number of Convolution layers 1→64 → 128 → 256 channels with activation functions ReLU + BatchNorm along with Two MaxPooling layers to downsample the spatial dimensions.
This results in millions of parameters, ensuring overparameterization of the model which is essential for this experiment.

We used Stochastic Gradient Descent (SGD) is a widely used optimization algorithm in Machine Learning having learnig rate of 0.02, momentum=0.9 and multiple weight decays so that effect of different weight decay can be seen.

Each Model is trained for 30 epochs and calculates training loss and accuracy of the model. This includes training accuracy, Test accuracy, Generaliztion Gap along with L2 weight norm over the time. 
## Run Locally

Clone the project
```bash
  git clone https://github.com/STILLADHIIKARII/FML-Project
```
Go to the project directory
```bash
  cd <your-repo>
```
Create and activate a virtual environment (optional but recommended)
```bash
    python -m venv venv
    source venv/bin/activate   # macOS/Linux
    venv\Scripts\activate      # Windows
```
Install dependencies
```bash
    pip install torch torchvision matplotlib
```
Launch Jupyter
```bash
    jupyter notebook
```
Open the notebook you want
```bash
    CNN-1kdatapoints.ipynb
    CNN-5k.ipynb
```
Run all cells in order
