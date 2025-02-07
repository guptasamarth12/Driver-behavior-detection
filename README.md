# 🚗 Driver Behavior Detection using CNNs

## 📌 About the Project
The **Driver Behavior Detection** project leverages **deep learning** to analyze images of drivers and classify their behavior. The goal is to automatically identify various driver activities—such as **safe driving, talking on the phone, texting, turning, and other distractions**—to enhance road safety and support the development of **intelligent transportation systems**.

---

## 📂 About the Dataset
The dataset consists of images categorized into **five** driver behavior classes:

- ✅ **Safe Driving**
- 📞 **Talking on the Phone**
- 💬 **Texting on the Phone**
- 🔄 **Turning**
- 🚦 **Other Activities**

### 🔹 Preprocessing Steps
To ensure high-quality input data for model training, the dataset was **preprocessed** using the following techniques:
- **Resizing**: Images were resized to **224x224 pixels** for uniformity.
- **Normalization**: Pixel values were scaled to the **[0,1]** range.
- **Data Augmentation**: Techniques such as **rotation, flipping, zooming, and brightness adjustments** were applied to enhance dataset variability and prevent overfitting.

---

## 🏗 Model Development
Three different **Convolutional Neural Network (CNN)** architectures were implemented and compared:

1️⃣ **AlexNet**  
2️⃣ **ResNet-34**  
3️⃣ **VGGNet (VGG-16 Variant)**  

Each model was trained on the dataset, and their performance was evaluated based on accuracy and loss.

---

## 🧠 Model Architectures
### 1️⃣ AlexNet
📌 **Architecture:**
- AlexNet consists of **5 convolutional layers**, followed by **3 fully connected layers**.
- It uses **ReLU activations, dropout layers for regularization, and max pooling layers**.

### 2️⃣ ResNet-34
📌 **Architecture:**
- ResNet-34 is a **34-layer deep network** that employs **residual (skip) connections** to tackle the **vanishing gradient problem**.
- It uses **3×3 convolution filters** throughout its residual blocks.

⚠ **Note:** ResNet-34 **underperformed** compared to the other models. The reason could be due to hyperparameter choices, dataset complexity, or insufficient fine-tuning.

### 3️⃣ VGGNet (VGG-16 Variant)
📌 **Architecture:**
- VGG-16 features a **deep but simple architecture** consisting of **multiple 3×3 convolution layers**, max pooling for downsampling, and fully connected layers at the end.
- This structure enables **deep feature extraction** while maintaining a manageable number of parameters.

---

## 📊 Model Performance Comparison

| Model       | Training Accuracy | Validation Accuracy | Training Loss | Validation Loss |
|-------------|-------------------|---------------------|---------------|-----------------|
| **AlexNet**  | 97.91%            | 96.21%              | 0.0262        | 0.0488          |
| **ResNet-34** | 46.82%           | 57.18%              | 1.2437        | 1.1431          |
| **VGGNet**   | 97.72%            | 98.94%              | 0.0567        | 0.0353          |

---

## 🔥 Key Takeaways
- **VGGNet performed the best** with the highest validation accuracy (**98.94%**) and lowest validation loss.
- **AlexNet also performed well**, achieving a **96.21% validation accuracy**.
- **ResNet-34 struggled to converge**, showing significantly lower accuracy (**57.18% validation accuracy**), likely due to improper hyperparameter tuning.

---

## 🚀 Future Improvements
To further improve the model, the following enhancements can be explored:
- **Hyperparameter tuning** (e.g., learning rate, batch size, dropout)
- **Implementing EfficientNet or MobileNet** for better performance with fewer parameters
- **Using a larger and more diverse dataset** for better generalization
- **Deploying the model** for real-time driver behavior monitoring using a webcam or mobile app

---

✅ **If you find this project useful, give it a ⭐ on GitHub!**  
