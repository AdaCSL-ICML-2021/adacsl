# Adaptive Cost-Sensitive Learning in Neural Networks for Misclassification Cost Problems


# Datasets
We host the datasets we used in the paper on the Kaggle platform.
- [Melanoma Classification: Harvard Dataverse (HAM10K)](https://www.kaggle.com/adacslicml/melanoma-classification-ham10k)
- [Breast   Histopathology   Images:(IDC)](https://www.kaggle.com/adacslicml/breast-histopathology-images)
- [Real   and   Fake   Face   Detection   (RFFD)](https://www.kaggle.com/adacslicml/real-and-fake-face-detection)
- [PlantVillage-Data Set (PV-D)](https://www.kaggle.com/adacslicml/plantvillagedata-set)

# Algorithms
In order to allow the reviewers to run all the algorithms and experiments that are described in the paper, we decided to present the code in the form of notebooks.
This configuration has several advantages.

Since GPU use is required (or at the very least, highly recommended) and we do not want to make assumptions about the hardware environment of the reviewers, 
notebooks can be used on the free Google Colab or Kaggle platforms.

In this way, the dependencies problem is also solved, and there is no need for the reviewers to adapt their work environment, create a new environment, or use tools like a Docker, in order to run the algorithms and experiments.

Also, even if the reviewers have a server with a GPU, it can be run remotely using an IDE like VSCode.

# Experimental Setup
In all experiments, we used pre-trained ResNet18, as implemented in PyTorch.

The batch size in the training phase is 64.

The maximum number of epochs ranges from 15 to 20 when selecting the test phase model is done as explained in the paper.
We use a Stochastic Gradient Descent as the optimizer.

The learning rate is 0.01 in most experiments, except when we saw that significant overfitting or underfitting occurred under the maximum number of epochs. In these cases, we modify the learning rate to 0.001 or 0.1.

Weight decay is 0.05, 0.01, or 0.01.
