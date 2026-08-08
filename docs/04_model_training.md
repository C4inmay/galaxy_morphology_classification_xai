# 04 - Model Training

## Model
- Architecture: ResNet18
- Pretrained weights: ImageNet
- Number of classes: 11
- Input size: 224 × 224
- Batch size: 32
- Optimizer: Adam
- Learning rate: 0.001
- Loss function: CrossEntropyLoss
- Device: Apple M1 MPS

## Training Strategy
The pretrained ResNet18 model was used for galaxy morphology classification.
The original feature extraction layers were frozen and only the final
fully connected classification layer was trained for the initial experiment.
Training was performed for 5 epochs using the Galaxy Zoo image dataset.

## Results

| Epoch | Train Loss | Train Accuracy | Val Loss | Val Accuracy |
|------:|-----------:|---------------:|---------:|-------------:|
| 1 | 1.7492 | 39.10% | 1.6964 | 39.87% |
| 2 | 1.6963 | 40.58% | 1.6748 | 41.63% |
| 3 | 1.6820 | 41.00% | 1.6926 | 40.56% |
| 4 | 1.6788 | 41.13% | 1.6734 | 42.10% |
| 5 | 1.6712 | 41.28% | 1.7097 | 39.97% |

## Best Result

- Best Validation Accuracy: **42.10%**
- Best Epoch: **4**
- Final Training Accuracy: **41.28%**
- Final Validation Accuracy: **39.97%**

## Observation

The initial model achieved approximately 42% validation accuracy.
Training accuracy increased gradually, while validation accuracy fluctuated.
The results indicate that the frozen-feature approach is not yet sufficient
for strong galaxy morphology classification. Further improvement will be
explored through fine-tuning, class balancing, and model optimization.

## Next Steps

1. Evaluate the trained model using precision, recall and F1-score.
2. Generate a confusion matrix.
3. Analyze incorrectly classified galaxies.
4. Fine-tune the pretrained model.
5. Apply SHAP/XAI for model interpretation.