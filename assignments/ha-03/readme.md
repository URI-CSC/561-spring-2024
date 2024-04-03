# Homework Assignment 3 (due Apr 10th @ 11:59pm)

For this assignment, you will tackle the *Caltech-101* image classification
problem using Convolutional Neural Networks (CNNs). Your tasks include:

- Transfer Learning: Leverage
[pre-trained models](https://pytorch.org/vision/stable/models.html) like
Inception, ResNet, or EfficientNet as a starting point, and fine-tune the
network on the provided dataset;

- Data Augmentation: Explore various data augmentation techniques, such 
as rotation, flipping, scaling, and color jittering, to artificially 
increase the size and diversity of the training data;

- Model Selection: Experiment with different CNN architectures, 
hyperparameters (e.g., learning rate, batch size, optimizer), and 
regularization techniques (e.g., dropout, weight decay) to 
find the best-performing model for the classification task.

You can work either locally on your machine or use the computational 
power of Google Colab's GPU runtime. Both options are acceptable, but 
using Colab might be more convenient if you don't have a powerful 
GPU on your local machine.

This is an individual assignment, and you are expected to complete it 
independently. However, you are encouraged to discuss general concepts 
and seek clarification from your instructors or peers if needed. 
Feel free to drop by our office hours or post your questions directly
on the `Ed Discussion` forum.

## The Dataset

The [*Caltech 101* dataset](https://data.caltech.edu/records/mzrjq-6wc02)
is a collection of pictures of objects 
belonging to 101 categories, with about 40 to 800 images per category. 
The size of each image is roughly `300x200` pixels. 

For this assignment you must download the following files:

- [training data](https://homepage.cs.uri.edu/~malvarez/stationary/caltech/train-files.zip)
- [training data labels](https://homepage.cs.uri.edu/~malvarez/stationary/caltech/train-labels.txt)
- [test data](https://homepage.cs.uri.edu/~malvarez/stationary/caltech/test-files.zip)

> [!NOTE]
> The labels for the training data appear in the same order as the
numbered file names given to the the training images.

## Hyperparameter Tuning

The recommended approach is to split your training data into training and
validation sets. You will train multiple models, each with a different
hyperparameter configuration. Then, you will select the model and hyperparameter
configuration that gives you the highest validation accuracy. Examples of 
hyperparameters include: choice of underlying pretrained model,
use of weight decay or dropout, choice of optimizer with their 
respective hyperparameters, and the batch size.  You may want to experiment
with your own architectures as well.

> [!TIP]
You are encouraged to used platforms like [Weights & Biases](https://www.wandb.com)
to keep track of your experiments and results. This will help you to better
understand the impact of different hyperparameters on the model's performance.

## Training a Final Model

After you are satisfied with the hyperparameter search, you will then train
a final model using all the data you have available (i.e., combine training
and validation data). You will use the hyperparameter configuration that gave
the highest validation accuracy during model selection. 

Once this final model is trained, you will use it to make predictions on the
provided test data. You will submit these predictions via *Gradescope*.
The predictions should be saved in a `torch` tensor of shape `(N, 101)`, 
where `N` is the number of test samples. Each row should contain the
predicted probabilities for each of the 101 classes. The order of the rows
should match the order of the test samples.

You can save a tensor using the `torch.save` function. For example:

```python
torch.save(predictions, 'predictions.pt')
```

## Submission and Grading

Once you are done with your work, you will submit the following files
via *Gradescope*:

> [!NOTE]
> You are strongly encouraged to include tables and charts in your report
> supporting each of the sections accordingly.

- your predictions for the test set in `predictions.pt`
- a PDF named `report.pdf` containing 4 sections, each with a clear 
description of how you implemented the following tasks:
    - transfer learning **(15 pt)**
    - data augmentation **(15 pt)**
    - hyperparameter tuning / model selection **(30 pt)**
    - training of the final model **(20 pt)**
- every source file you developed (only `.py` and `.ipynb` files are allowed) **(20 pt)**

> [!CAUTION]
> Remember, academic integrity is of utmost importance.  Any attempts at cheating
> or plagiarism will result in a forfeiture of credit.
