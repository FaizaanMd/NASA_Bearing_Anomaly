# 🔧 Bearing Failure Detection Using Anomaly Detection Techniques

This project presents a comprehensive pipeline for detecting bearing failures using statistical analysis and machine learning-based anomaly detection techniques. Vibration sensor data from test-to-failure experiments is processed to identify early signs of bearing degradation.

The solution incorporates advanced techniques such as Isolation Forest, One-Class SVM, Local Outlier Factor, Autoencoders, to detect anomalies across three separate bearing test datasets.

---

## 🎯 Project Objectives

- 📥 **Data Acquisition & Preprocessing:** Ingest raw vibration signal data and apply cleaning procedures.
- 📈 **Feature Engineering:** Extract time-domain statistical features to represent vibration signals effectively.
- 🧠 **Model Development:** Apply multiple unsupervised anomaly detection algorithms to identify failure events.
- 📊 **Performance Evaluation:** Assess and compare detection accuracy, false positives, and signal trends.
- 🔍 **Failure Insight:** Interpret anomalies in the context of known bearing failures.

---

## 📚 Dataset Overview

The dataset comprises vibration signals collected during real-world degradation of bearings under controlled experimental conditions.

### ▪ Test Set 1
- **Duration:** Oct 22 – Nov 25, 2003  
- **Files:** 2,156 (ASCII format)  
- **Channels:** 8  
- **Failure Type:**  
  - Bearing 3: Inner race defect  
  - Bearing 4: Roller element defect  

### ▪ Test Set 2
- **Duration:** Feb 12 – Feb 19, 2004  
- **Files:** 984  
- **Channels:** 4  
- **Failure Type:**  
  - Bearing 1: Outer race defect  

### ▪ Test Set 3
- **Duration:** Mar 4 – Apr 4, 2004  
- **Files:** 4,448  
- **Channels:** 4  
- **Failure Type:**  
  - Bearing 3: Outer race defect  

---

## 🧠 Anomaly Detection Models

| Model                | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| **Isolation Forest** | Tree-based method that isolates anomalies as outliers in random partitions |
| **One-Class SVM**    | Learns a boundary around normal data to detect novelties                    |
| **Local Outlier Factor (LOF)** | Measures local deviation of density for each data point      |
| **Autoencoders**     | Neural networks that reconstruct normal signals and detect anomalies via reconstruction error |

---

## 🔬 Key Observations

- **Test Set 1:** Anomalies appear progressively, correlating with documented defects in Bearings 3 and 4.  
- **Test Set 2:** Sharp vibration increase in Bearing 1 indicates outer race failure.  
- **Test Set 3:** Late-stage anomaly spikes suggest outer race degradation in Bearing 3.

---

## 📈 Experimental Results

| Model                  | Test Set 1       | Test Set 2         | Test Set 3         |
|------------------------|------------------|---------------------|---------------------|
| Isolation Forest       | High Precision   | High Precision      | High Precision      |
| One-Class SVM          | High False Pos.  | Tuned Effectively   | Tuned Effectively   |
| Local Outlier Factor   | Requires Tuning  | Effective w/ tuning | Effective w/ tuning |
| Autoencoders           | Best Performance | Best Performance    | Best Performance    |
---

## 🛠 Technology Stack

- **Python Libraries:** `NumPy`, `Pandas`, `Scikit-learn`, `TensorFlow`, `Matplotlib`, `Seaborn`
- **Development Environment:** Google Colab    

---

## 🚀 Execution Pipeline

1. **Environment Setup**
   - Use Google Colab or local Python 3 environment
   - Install required libraries via `pip`

2. **Dataset Acquisition**
   - Download and extract test data (ASCII files)

3. **Data Preprocessing**
   - Parse raw signals
   - Normalize and structure the data

4. **Feature Extraction**
   - Compute time-domain features:
     - Mean, Standard Deviation, Skewness, Kurtosis, Entropy, RMS, Peak-to-Peak

5. **Model Training & Evaluation**
   - Train anomaly detection models on extracted features
   - Visualize and compare anomaly results

6. **Output Generation**
   - Save results as `.csv`
   - Generate time-series plots with anomaly overlays

---

## 📁 Project Structure

```plaintext
Root/
├── Data/
│   ├── 1st_test/
│   ├── 2nd_test/
│   ├── 3rd_test/
├── ProcessedData/
│   ├── MergedData/
│   ├── Test1_TimeFeatures.csv
│   ├── Test2_TimeFeatures.csv
│   ├── Test3_TimeFeatures.csv
├── AnomalyDetection/
│   ├── BearingTest_1_Anomalies.csv
│   ├── BearingTest_2_Anomalies.csv
│   ├── BearingTest_3_Anomalies.csv
└── Readme Document for IMS Bearing Data.pdf
```

## 🔖 License

This project is provided for educational and research purposes. Please reference the original dataset source for any publication or presentation.

## 👤 Author

**Md Faizaan**  
[LinkedIn](https://www.linkedin.com/in/faizaan-md-449064358/) | [GitHub](https://github.com/FaizaanMd)

Feel free to reach out if you have any questions or feedback regarding this project.


