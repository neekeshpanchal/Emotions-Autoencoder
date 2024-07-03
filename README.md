# **Emotions-Autoencoder**

![Emotions-Autoencoder](https://github.com/neekeshpanchal/Emotions-Autoencoder/assets/80868396/046f0cc2-20f2-4091-9e67-8b00e6f90aad)

**Harnessing the Power of Autoencoders and Sequential Neural Networks to Predict Human Emotions in Video**

---

## 🚀 **Project Overview**

Emotions-Autoencoder applies cutting-edge machine learning techniques to predict human emotions in video frames. Leveraging the power of Keras, sklearn, matplotlib, and OpenCV, this project demonstrates a robust approach to real-time emotion detection.

---

## 🧠 **Model Architecture**

### **Encoder Layer:**

```
Layer (type)                Output Shape              Param #   
=================================================================
Input Layer                [(None, 64, 64, 3)]        0         
Conv2D (32 filters)        (None, 64, 64, 32)         896       
MaxPooling2D               (None, 32, 32, 32)         0         
Conv2D (16 filters)        (None, 32, 32, 16)         4624      
MaxPooling2D               (None, 16, 16, 16)         0         
Conv2D (8 filters)         (None, 16, 16, 8)          1160      
MaxPooling2D               (None, 8, 8, 8)            0         
Conv2D (8 filters)         (None, 8, 8, 8)            584       
UpSampling2D               (None, 16, 16, 8)          0         
Conv2D (16 filters)        (None, 16, 16, 16)         1168      
UpSampling2D               (None, 32, 32, 16)         0         
Conv2D (32 filters)        (None, 32, 32, 32)         4640      
UpSampling2D               (None, 64, 64, 32)         0         
Conv2D (3 filters)         (None, 64, 64, 3)          867       
=================================================================
Total params: 13,939
Trainable params: 13,939
Non-trainable params: 0
```

### **Sequential Model:**

```
Layer (type)                Output Shape              Param #
=================================================================
Flatten                    (None, 12288)              0
Dense (128 units)          (None, 128)                1,572,992
Dense (64 units)           (None, 64)                 8,256
Dense (3 units)            (None, 3)                  195
=================================================================
Total params: 1,581,443
Trainable params: 1,581,443
Non-trainable params: 0
```

---

## 📊 **Visualization and Results**

![Visualization](https://github.com/neekeshpanchal/Emotions-Autoencoder/assets/80868396/046f0cc2-20f2-4091-9e67-8b00e6f90aad)

Our model is designed to detect and visualize the latent features of emotions across video frames. The PCA visualization provides an intuitive understanding of the model's performance in distinguishing between different emotions.

---

## 📂 **Project Structure**

```
├── data
│   ├── Angry
│   ├── Happy
│   └── Sad
├── models
│   ├── encoder.h5
│   ├── emotion_classifier.h5
├── notebooks
│   ├── Data_Preprocessing.ipynb
│   ├── Model_Training.ipynb
├── scripts
│   ├── train_autoencoder.py
│   ├── train_classifier.py
│   ├── video_emotion_gui.py
├── README.md
```

---

## 📚 **Installation and Usage**

### **1. Clone the Repository:**

```sh
git clone https://github.com/neekeshpanchal/Emotions-Autoencoder.git
cd Emotions-Autoencoder
```

### **2. Install Dependencies:**

```sh
pip install -r requirements.txt
```

### **3. Run the Application:**

```sh
python scripts/video_emotion_gui.py
```

---

## 🤖 **Future Work**

- **Integration with Real-time Streaming:** Implement live emotion detection on video streams.
- **Enhanced Emotion Categories:** Expand the model to detect a broader range of emotions.
- **Optimized Model Performance:** Further refine the model for faster and more accurate predictions.

---

## 🎓 **Contributors**

- [Neekesh Panchal](https://github.com/neekeshpanchal)

---

## 📜 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Feel free to explore, contribute, and share your feedback! Together, let's make emotion detection smarter and more accessible.**

![Footer Image](https://github.com/neekeshpanchal/Emotions-Autoencoder/assets/80868396/046f0cc2-20f2-4091-9e67-8b00e6f90aad)

