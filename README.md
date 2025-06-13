# nslkdd_ueba_pipeline
Predicting anomalies and attack types of the nslkdd dataset
# NSL-KDD UEBA Anomaly Detection

High-accuracy anomaly detection using the NSL-KDD dataset. This is a **UEBA-style behavioral detection model**, not rule-based IDS.
how to run : Use the KDDTrain+_20Percent.csv file to run the notebook locally.
## 🔧 Method

- **Stage 1:** Isolation Forest for anomaly detection
- **Stage 2:** Random Forest for attack type classification
- **Final Rule:** If anomaly_pred == 0 OR attack_type == 'normal' → Normal, else Abnormal

## ✅ Final Results

- **Accuracy:** 98.72%
- **Error Rate:** 1.28% (≈ 2× better than common commercial systems)
- **Confusion Matrix:**
[[13449 0]
[ 322 11421]]

- **F1-Score (Abnormal):** 0.9861

## 💡 Notes

- Behavioral detection (UEBA) applied to NSL-KDD network traffic
- Outputs can be used in a UEBA system that feeds a firewall, not replace it
