🚗 Driver Behavior Detection using CNNs
📌 About the Project
This project leverages deep learning techniques to analyze images of drivers and classify their behavior. The goal is to automatically detect various driver activities—such as safe driving, talking on the phone, texting, turning, and other distractions—to enhance road safety and support the development of intelligent transportation systems.

📂 About the Dataset
The dataset consists of images categorized into five classes:

Safe Driving
Talking on the Phone
Texting on the Phone
Turning
Other Activities
To ensure robustness, the dataset was collected under diverse conditions, including variations in angles, lighting, and environments. The preprocessing steps applied include:

Resizing: All images were resized to a uniform dimension (e.g., 224×224 pixels).
Normalization: Pixel values were scaled to the range [0, 1] to enhance training stability.
Data Augmentation: Techniques such as rotation, flipping, and zooming were applied to increase dataset variability and prevent overfitting.
🔧 Model Development
Three different Convolutional Neural Network (CNN) architectures were implemented and compared:

AlexNet
ResNet-34
VGGNet (VGG-16 Variant)
📌 Model Architectures
🔹 AlexNet
AlexNet consists of five convolutional layers followed by three fully connected layers. It employs:
✅ ReLU activations for non-linearity
✅ Max pooling layers for downsampling
✅ Dropout for regularization

🔹 ResNet-34
ResNet-34 is a 34-layer deep network that introduces residual connections (skip connections) to combat the vanishing gradient problem. It maintains simple 3×3 convolution filters throughout its residual blocks.

⚠️ Note: ResNet-34 underperformed compared to the other models. This could be due to hyperparameter choices, dataset complexity, or insufficient fine-tuning.

🔹 VGGNet (VGG-16 Variant)
VGG-16 follows a structured design of stacked 3×3 convolutional layers, interleaved with max pooling layers, and ending with fully connected layers. This model is known for its simplicity and effectiveness in image classification tasks.

📊 Model Performance Comparison
Model	Training Accuracy	Validation Accuracy	Training Loss	Validation Loss
AlexNet	97.91%	96.21%	0.0262	0.0488
ResNet-34	46.82%	57.18%	1.2437	1.1431
VGGNet	97.72%	98.94%	0.0567	0.0353
🏆 Conclusion
VGGNet achieved the highest validation accuracy (98.94%), making it the best-performing model for this task.
AlexNet also performed well, with a validation accuracy of 96.21%, making it a competitive choice.
ResNet-34, despite being a deeper model, had lower accuracy, likely due to insufficient fine-tuning or dataset-related challenges.
This project demonstrates how different CNN architectures perform in driver behavior classification. Future improvements could include:
✅ Exploring other deep learning models (EfficientNet, MobileNet, or Transformer-based models).
✅ Fine-tuning hyperparameters and using transfer learning.
✅ Expanding the dataset with more diverse real-world images.
