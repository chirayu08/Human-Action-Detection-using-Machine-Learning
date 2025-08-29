# Human Activity Recognition using Mobile Health Sensor Data

## 📌 Overview
This project uses **Mobile Health (mHealth) sensor data** to classify **human activities** such as walking, running, sitting, climbing stairs, cycling, etc., using machine learning algorithms.

The dataset contains accelerometer and gyroscope readings from multiple body locations, along with activity labels.  
Our model learns from these signals to predict the performed activity.

---

## 📊 Dataset
The dataset is sourced from Kaggle:  
📂 **[Mobile Health Dataset](https://www.kaggle.com/datasets/gaurav2022/mobile-health)**  

### Dataset Description:
- **Sensors**: Accelerometer, Gyroscope
- **Positions**: Left ankle, right wrist
- **Subjects**: Multiple human participants
- **Activities**:
    - None
    - Standing still (1 min)
    - Sitting and relaxing (1 min)
    - Lying down (1 min)
    - Walking (1 min)
    - Climbing stairs (1 min)
    - Waist bends forward (20x)
    - Frontal elevation of arms (20x)
    - Knees bending (crouching) (20x)
    - Cycling (1 min)
    - Jogging (1 min)
    - Running (1 min)
    - Jump front & back (20x)

---

## ⚙️ Installation & Setup
### 1. Clone the Repository
```bash
git clone https://github.com/<your-username>/mhealth-activity-recognition.git
cd mhealth-activity-recognition
````

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Download Dataset

Download the dataset from Kaggle:

```bash
kaggle datasets download -d gaurav2022/mobile-health
unzip mobile-health.zip
```

Ensure the CSV file (`mhealth_raw_data.csv`) is in the project directory.

### What the Code Does:

1. **Load Dataset** from CSV.
2. **Data Exploration** – Check missing values, duplicates, activity counts.
3. **Balancing Data** – Sample "None" class to avoid imbalance.
4. **Activity Visualization** – Plot line charts & histograms for each activity.
5. **Data Cleaning** – Remove outliers using the 1st & 99th percentile range.
6. **Feature Scaling** – Robust Scaler to normalize sensor readings.
7. **Model Training** – Multiple ML algorithms tested:
   * Logistic Regression
   * K-Nearest Neighbors (KNN)
   * Decision Tree
   * Support Vector Machine (SVM)
   * Naive Bayes
   * Random Forest (and can be extended to XGBoost, LightGBM, etc.)
8. **Evaluation** – Confusion matrix, accuracy, precision, recall, F1-score.
---

## 📈 Example Output

* **Activity Distribution**
* **Confusion Matrix**
* **Performance Metrics** for each model.

---

## 💡 Real-Life Applications

* **Healthcare Monitoring** – Fall detection, patient movement tracking.
* **Fitness Tracking** – Step counting, exercise detection.
* **Workplace Safety** – Monitoring unsafe movements in factories.
* **Smart Homes** – Activity-based automation.
* **Sports Science** – Analysing training movements.

---

## 📌 Future Improvements

* Add **CNN/LSTM** models for time-series classification.
* Implement **real-time activity recognition** from wearable devices.
* Use **XGBoost / LightGBM** for improved accuracy.
* 
## 📜 License
This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.
## 🙌 Acknowledgements

##updated code with more models

https://colab.research.google.com/drive/10XzVaQ5Be3PlxV9bPqlQb1ri2i7-knsU?usp=sharing

Dataset: [Mobile Health Dataset](https://www.kaggle.com/datasets/gaurav2022/mobile-health) by Gaurav2022
Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`
