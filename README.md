# 🎯 Exploring CNN Architectures on CIFAR-10

In this project, I experimented with **Convolutional Neural Networks (CNNs)** on the **CIFAR-10 dataset**.  
The focus was to analyze how different architectural choices and training strategies impact model performance.

---

## 🏗️ Network Architecture
The main CNN model consisted of:
- **Conv2D (32 filters, kernel size 5×5, ReLU)** + BatchNorm  
- **Conv2D (32 filters, kernel size 3×3, ReLU)** + BatchNorm  
- **MaxPooling2D (2×2)**  
- **Conv2D (68 filters, kernel size 3×3, ReLU)** + BatchNorm  
- **Conv2D (68 filters, kernel size 3×3, ReLU)** + BatchNorm  
- **MaxPooling2D (2×2)**  
- **Flatten → Dense (128 units, ReLU) → Dropout(0.3) → Dense (10 units, Softmax)**  

---

## ⏱️ Training Experiments
I tested the model under different setups (50 epochs each):  
- ✅ **With Pooling Layer** → Faster training and higher accuracy.  
- ❌ **Without Pooling Layer** → Slower training, lower accuracy.  
- ⚡ **Stride Comparison (2 vs 4)** in pooling:  
  - Stride = 2 → better accuracy and stable training.  
  - Stride = 4 → information loss, lower accuracy.  
- 📉 **Schedulers (Exponential vs OneCycle)**:  
  - Exponential Decay → slower but stable convergence.  
  - OneCycle Policy → faster convergence, improved final accuracy.  

---

## ✅ Key Takeaways
- Pooling layers play a **critical role** in reducing training time and improving accuracy.  
- Proper stride selection (e.g., 2 instead of 4) significantly improves performance.  
- The **OneCycle Scheduler** outperformed Exponential Decay in both speed and accuracy.  
- CNNs proved to be **efficient and effective** on CIFAR-10 classification tasks.  

---

🔗 Excited to keep exploring **Deep Learning** and **Computer Vision**.  
I’d love to hear your thoughts and experiences with CNNs on image datasets!
