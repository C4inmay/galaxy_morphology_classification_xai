# Data Preparation for Deep Learning

## Objective

Prepare the Galaxy Zoo dataset for deep learning by converting labels into numerical values, splitting the dataset, applying image preprocessing, and creating an efficient PyTorch data pipeline.

---

## Label Encoding

The final galaxy classes were converted into numerical labels using Scikit-learn's `LabelEncoder`. Neural networks require numerical targets instead of text labels, making this step essential for model training. A label mapping was also generated to translate predictions back into human-readable class names.

---

## Train-Validation Split

The dataset was divided into 80% training and 20% validation using a stratified split. Stratification preserved the class distribution across both subsets, ensuring that each galaxy class was represented proportionally during training and evaluation.

---

## Image Preprocessing

All images were resized from **424×424** to **224×224**, which matches the input size expected by ResNet18. Data augmentation techniques such as random horizontal flipping and small rotations were applied only to the training images to improve model generalization. Finally, images were converted into tensors and normalized using ImageNet statistics.

---

## Custom PyTorch Dataset

A custom `GalaxyDataset` class was implemented by inheriting from PyTorch's `Dataset`. This class loads an image using its `GalaxyID`, applies the required transformations, and returns the processed image together with its encoded label. This provides a reusable and scalable way to access the dataset during training.

---

## DataLoader

PyTorch `DataLoader`s were created for both the training and validation datasets using a batch size of 32. The training loader shuffles the data every epoch to improve learning, while the validation loader preserves the original order for consistent evaluation. The data pipeline was verified by successfully loading image batches of shape **(32, 3, 224, 224)**.

---

## Outcome

The complete deep learning data pipeline has been successfully prepared. The project is now ready for model development using a pretrained ResNet18 architecture.