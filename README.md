# SmartShelf — Explainable AI Food Quality & Shelf-Life Prediction System

SmartShelf is an end-to-end computer vision based system that analyzes food images and predicts:

• Food Category
• Freshness Stage (Fresh / Mid / Spoiled)
• Estimated Remaining Shelf Life (in days)

The system supports multiple food groups including vegetables, fruits, meat & seafood, and bakery products using specialized deep learning models.

Unlike traditional classifiers, SmartShelf integrates Explainable AI to show WHY the model considers food spoiled, improving reliability and user trust.

The goal of this project is to reduce food waste and enable intelligent storage systems such as smart refrigerators and retail monitoring solutions.

---

## 🚀 Features

• Multi-food support (Vegetables, Fruits, Meat/Seafood, Bakery)
• Category-specific deep learning models
• Freshness classification
• Shelf-life regression prediction
• Explainable AI visualization (LIME & Grad-CAM)
• Interactive web interface
• Live deployment using Ngrok

---

## 🧠 Model Architecture

Instead of a single model, SmartShelf uses a category-aware multi-model approach:

| Food Category | Model Used |
|-------------|------|
| Vegetables | EfficientNet-B0 |
| Fruits | MobileNet |
| Meat & Seafood | EfficientNet-B4 |
| Bread/Bakery | MSFFS |

The system detects the food category and routes the image to the appropriate model for accurate spoilage prediction.

---

## 🔍 Explainable AI (Model Interpretability)

To ensure transparency and trust, SmartShelf integrates Explainable AI techniques:

### Grad-CAM
Highlights image regions responsible for the prediction  
Helps visualize spoilage areas such as discoloration, mold, or texture changes

### LIME (Local Interpretable Model-Agnostic Explanations)
Provides local explanations for each prediction  
Shows which parts of the food influenced classification

This allows users to understand WHY the system marked food as spoiled instead of only seeing a prediction.

---

## 🗂 Dataset Structure

Dataset is organized using time-progressive labeling to simulate real spoilage:

dataset/
    vegetables/
        tomato/day1/
        tomato/day3/
        tomato/day5/
    fruits/
    meat_seafood/
    bakery/

This helps the model learn natural freshness decay rather than manual annotation.

---

## 🛠 Tech Stack

Python  
Deep Learning (CNN)  
Computer Vision  
Explainable AI (LIME, Grad-CAM)  
Streamlit  
Ngrok  
Google Colab

Libraries:
TensorFlow / PyTorch
OpenCV
NumPy
Pandas
Matplotlib

---

## 💻 Installation


1. Install dependencies

pip install -r requirements.txt

2. Run application

streamlit run app.py

3. Enable public access (optional)

ngrok http 8501

---

## 📊 How It Works

1. Upload food image in specific category
2. Model predicts freshness stage
3. Shelf life estimated in days
4. Grad-CAM & LIME explanations generated
5. Result displayed on dashboard

---

## 🌍 Applications

• Smart Refrigerators
• Supermarket Inventory Monitoring
• Food Waste Reduction Systems
• Household Food Management

---

## 🔮 Future Improvements

• Mobile application integration
• Real-time camera detection
• IoT refrigerator sensors
• Expiry alert notifications

---

## 👩‍💻 Author

Archana

---

## ⭐ Support

If you like this project, give it a star ⭐ on GitHub!
