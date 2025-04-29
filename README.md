Dog vs Cat Classifier 🐾
A Binary Image Classification project that distinguishes dogs from cats using transfer learning with MobileNetV2. The model is fine-tuned for higher performance on a custom dataset.

🔧 Tech Stack
Python

TensorFlow / Keras

MobileNetV2 (Pretrained on ImageNet)

Binary Classification (Sigmoid activation)

📁 Folder Structure
kotlin
Copy
Edit
.
├── dog_cat_classifier.py     # Main script
├── data/
│   ├── train/
│   │   ├── cats/
│   │   └── dogs/
│   └── val/
│       ├── cats/
│       └── dogs/
└── README.md

🚀 Getting Started
Install Requirements
bash
Copy
Edit
pip install tensorflow numpy matplotlib
Train the Model
bash
Copy
Edit
python dog_cat_classifier.py

⚙️ Model Architecture
Pretrained MobileNetV2 as base (frozen initially)

GlobalAveragePooling2D

Dense layer with ReLU

Dropout for regularization

Final Dense layer with Sigmoid (Binary Output)

🔁 Training Strategy
Initial Training with frozen MobileNetV2

Fine-Tuning: Unfreeze top layers to improve performance

python
Copy
Edit
model.compile(loss='binary_crossentropy', optimizer='adam', metrics=['accuracy'])
🎯 Output
Accuracy after fine-tuning: ~93%

Binary prediction: 0 = Cat, 1 = Dog

📸 Sample Prediction
python
Copy
Edit
model.predict(img_array)
# Output: [[0.983]] → Dog
🙋‍♂️ Author
Jaiselvan R
