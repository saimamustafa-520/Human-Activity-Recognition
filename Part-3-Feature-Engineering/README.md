Files:

code.ipynb – Feature extraction, training, evaluation

har_features.csv – Saved features

fcnn_model.pth – Trained model


Data: 6 activity classes, features scaled, 80/20 train-validation split.

FCNN: 128 → 64 → 32 hidden layers (ReLU), 6 output neurons, Cross-Entropy Loss, Adam, batch 32, 50 epochs.

Results: Accuracy ~68.4%, F1 ~0.673; better than classical ML (~57%). No major overfitting/underfitting.

Usage: Run code.ipynb. Load model for inference:

model = FCNN(16,6)
model.load_state_dict(torch.load("fcnn_model.pth"))
model.eval()

Limitations: Temporal patterns not fully captured; accuracy can improve with deeper or sequence models.
