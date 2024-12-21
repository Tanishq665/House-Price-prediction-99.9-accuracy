# **House Price Prediction with Ensemble Learning**

This repository provides a Python-based solution for predicting house prices using an ensemble model of Random Forest and XGBoost. The solution is optimized for both performance and accuracy, with support for GPU acceleration and a user-friendly interface built using Gradio.

---

## **Features**

### **1. Ensemble Learning**
- Combines **Random Forest** and **XGBoost** to ensure robust and accurate predictions.
- Hyperparameter tuning using GridSearchCV for optimal model performance.

### **2. Interactive User Interface**
- Built with **Gradio**, allowing users to input custom data via an intuitive interface.
- Accepts the following inputs:
  - Layout Type (BHK or RK)
  - Property Type (Apartment or Independent House)
  - Furnish Type (Furnished, Semi-Furnished, Unfurnished)
  - City (e.g., Mumbai, Bangalore)
  - Area (in square feet)
  - Number of Bedrooms and Bathrooms
- Displays predicted house prices in real-time.

### **3. Model Performance Evaluation**
- Evaluates models with metrics such as:
  - **Root Mean Squared Error (RMSE)**
  - **R² Score**
- GPU-accelerated training for faster computations.

### **4. Model Persistence**
- Save and load trained models using **Pickle**, avoiding the need for retraining after runtime resets.

---

## **Getting Started**

### **1. Setup Environment**
Ensure the following dependencies are installed:
```bash
pip install -r requirements.txt
```

For GPU acceleration (optional):
- Enable GPU runtime (e.g., NVIDIA T4 GPU in Google Colab).
- Ensure CUDA-compatible versions of libraries are installed.

### **2. Train the Model**
Train the ensemble model on your dataset:
```bash
python train.py
```

### **3. Save the Trained Model**
Save the trained model to a file:
```bash
python save_model.py
```

### **4. Load the Saved Model**
Load the model for making predictions:
```bash
python load_model.py
```

### **5. Run Gradio Interface**
Launch the Gradio app for interactive predictions:
```bash
python app.py
```

---

## **Dataset Format**

Ensure the dataset includes the following features:
- **Number of Bedrooms** (e.g., 2, 3)
- **Layout Type** (e.g., BHK, RK)
- **Property Type** (e.g., Apartment, Independent House)
- **Furnish Type** (e.g., Furnished, Semi-Furnished, Unfurnished)
- **City** (e.g., Mumbai, Bangalore)
- **Area** (in square feet)
- **Number of Bathrooms**
![Screenshot (115)](https://github.com/user-attachments/assets/8b3cc277-578d-4cea-9fa0-d4bfa027f760)

Preprocess the dataset to include derived features such as:
- **Log-transformed Area**
- **Price per Square Foot**

---

## **Performance Metrics**
![Screenshot (114)](https://github.com/user-attachments/assets/aa1092a2-92e8-41f3-aa05-4e6d06d6e68f)

- **Root Mean Squared Error (RMSE)**: ₹00.01
- **R² Score**: 0.9998

---

## **Optimization Tips**

- Use GPU runtime for faster training (XGBoost is configured with `tree_method='gpu_hist'`).
- Adjust hyperparameters such as:
  - `max_depth`: Maximum depth of the trees
  - `min_samples_split`: Minimum number of samples required to split an internal node
  - `learning_rate`: Step size shrinkage for XGBoost

---

## **Future Enhancements**

- Include additional features like locality and amenities.
- Experiment with neural networks for enhanced accuracy.
- Integrate APIs for real-time data fetching and predictions.

---

## **Contributors**
- **Tanishq Pahuja** (Project Develop)

Feel free to fork, contribute, or raise issues for improvement!

---

## **License**

This project is licensed under the MIT License. See the LICENSE file for details.

