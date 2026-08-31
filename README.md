
# Fine-Tuning ResNet50 Pretrained on ImageNet for CIFAR-10

We explored the process of fine-tuning a pretrained ResNet50 model on the CIFAR-10 dataset. The ResNet50 model was adapted for CIFAR-10 by modifying the first convolutional layer and replacing the final classification layer with a 10-class output layer.

## Hyperparameters

- Model: ResNet50 pretrained on ImageNet
- Optimizer: Stochastic Gradient Descent (SGD)
- Learning rate: 0.01
- Momentum: 0.9
- Weight decay: 5e-4
- Learning-rate scheduler: Cosine Annealing
- Scheduler T_max: 200
- Epochs: 60
- Number of classes: 10

## Results

The fine-tuned ResNet50 achieved an accuracy of **92.34%** on the CIFAR-10 test set.

When the batch size was increased from 32 to 64, an accuracy of **92.63%** was achieved.

- **Training Accuracy:** Increased from 53.80% in the first epoch to 90.64% in the final epoch.
- **Training Loss:** Decreased from 1.3067 to 0.2779.
- **Testing Accuracy:** Improved from 69.60% to 87.68% during training.
- **Test Loss:** Decreased from 0.8660 to 0.3625.

## Key Takeaways

- Fine-tuning an ImageNet-pretrained ResNet50 is effective for CIFAR-10 classification.
- The first convolutional layer was modified to better handle CIFAR-10's 32×32 images.
- The final classification layer was replaced with a 10-class classifier.
- Cosine Annealing was used for learning-rate scheduling.
- Increasing the batch size from 32 to 64 improved the reported accuracy from **92.34% to 92.63%**.

## Project Structure

- `Fine-Tuning-ResNet50-Pretrained-on-ImageNet-for-CIFAR-10.ipynb` — training and evaluation notebook
- `README.md` — project documentation
