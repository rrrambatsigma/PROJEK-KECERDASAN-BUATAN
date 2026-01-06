
---

# 🧠 Learning Space Comfort Recommendation System using Mamdani Fuzzy Inference

This project implements a **Mamdani Fuzzy Inference System (FIS)** to evaluate and recommend the most comfortable learning spaces at **Universitas Sebelas Maret (UNS)** based on real environmental conditions on two places FATISDA (Fakultas Teknologi Informasi dan Sains Data) dan FMIPA (Fakultas Matematika dan Ilmu Pengetahuan Alam).

The system processes uncertain physical parameters such as temperature, humidity, noise level, and Wi-Fi signal strength to generate a comfort score and learning space recommendation.

---

## 📌 Project Overview

The physical learning environment strongly affects student productivity and concentration. This research designs a **Fuzzy Inference System (Mamdani method)** to determine the comfort level of study spaces at **FMIPA and FATISDA UNS**.

Data were collected from **7 campus locations** across **three time periods**:

* Morning
* Midday
* Afternoon

Each record is evaluated using fuzzy logic to produce a comfort score from **0–10**, classified into:

| Score Range | Category      |
| ----------- | ------------- |
| 0.0 – 4.2   | Uncomfortable |
| 3.8 – 7.1   | Fair          |
| 6.8 – 10.0  | Comfortable   |

---

## 🧪 Input Variables

| Variable       | Unit | Fuzzy Sets           |
| -------------- | ---- | -------------------- |
| Temperature    | °C   | Cold, Moderate, Hot  |
| Humidity       | %    | Dry, Moderate, Humid |
| Noise Level    | dB   | Low, Medium, High    |
| Wi-Fi Strength | dBm  | Weak, Medium, Strong |

---

## 🔄 System Workflow

1. **Data Collection**
   Environmental data were measured using:

   * Room thermometer
   * Online decibel meter
   * Wi-Fi signal strength app

2. **Preprocessing**

   * Merge all sensor data
   * Handle missing values using mean imputation

3. **Fuzzification**
   Convert crisp values into fuzzy membership degrees.

4. **Rule Inference (Mamdani)**

   * Implication: **MIN operator**
   * Aggregation: **MAX operator**

5. **Defuzzification**

   * Method: **Centroid of Area (CoA)**
   * Output: Comfort Score (0–10)

---

## 📜 Example Fuzzy Rules

* IF *Temperature is Moderate* AND *Noise is Low* → **Comfortable**
* IF *Noise is High* → **Uncomfortable**
* IF *Wi-Fi is Weak* AND *Noise is Medium or High* → **Uncomfortable**

---

## 📊 Key Findings

* **Morning** is the most comfortable time for studying due to:

  * Moderate temperature
  * Low noise level

* **Midday and Afternoon** are dominated by **Uncomfortable** scores because of:

  * High temperature
  * High noise intensity

* **Noise Level** is the most dominant factor.

* **Temperature** determines the baseline comfort potential.

* **Wi-Fi and Humidity** act as secondary factors.

---

## 🏆 Best Study Locations

| Time      | Recommended Location | Score | Category      |
| --------- | -------------------- | ----- | ------------- |
| Morning   | FATISDA – Indoor     | 7.29  | Comfortable   |
| Midday    | FATISDA – Outdoor    | 3.73  | Uncomfortable |
| Afternoon | FATISDA – Indoor     | 3.27  | Uncomfortable |

**FATISDA Indoor** is the most consistent location across all time periods.

---

## 🛠 Technologies

* Python / MATLAB (FIS Implementation)
* Mamdani Fuzzy Logic
* Centroid Defuzzification
* Environmental Sensing Tools

---

## 🎯 Conclusion

This project proves that the **Mamdani Fuzzy Inference System** effectively handles uncertainty in environmental data and provides realistic comfort evaluations.
The model can be further developed into a **smart campus recommendation system** to help students choose optimal study spaces dynamically.

---

## 👨‍🎓 Authors

* Rambat Ungu Aryati
* Dien Akmalin Rizki Akbar
* Fatih Dzaki Nabhani

Data Science – Universitas Sebelas Maret

---

