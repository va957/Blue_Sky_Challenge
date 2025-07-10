# **Temporal Forecasting of CO and Temperature – Blue Sky Hackathon**

## **Project Overview**

This project leverages **time series forecasting** techniques to predict **temperature** and **carbon monoxide (CO)** levels using historical data. The goal is to predict future air quality measurements to enhance **smart air quality monitoring systems**. The project employs a combination of **statistical modeling** with **ARIMA** and **deep learning** with **LSTM** (Long Short-Term Memory) and **GRU** (Gated Recurrent Units) layers to achieve accurate predictions.

---

## **Table of Contents**

- [Project Objective](#project-objective)
- [Methodology](#methodology)
- [Technologies Used](#technologies-used)
- [Model Performance](#model-performance)
- [Results and Graphs](#results-and-graphs)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

---

## **Project Objective**

The primary objective of this project is to forecast daily **temperature** and **CO** levels based on the historical data of the past 7 days. By implementing advanced **time series techniques**, the model predicts the **8th, 9th, 10th**, and subsequent days’ air quality data. This forecasting aims to provide valuable insights for **smart environmental monitoring systems** and **air quality management**.

---

## **Methodology**

The project uses a **hybrid approach** combining **ARIMA** for statistical analysis and **LSTM** with **GRU** layers for **deep learning-based predictions**.

### **1. Data Preprocessing:**
   - Data from past days (7 days of CO and temperature records) were used for training.
   - **Missing values** were handled through **linear interpolation**.
   - The dataset was split into **training** and **testing datasets** for validation.

### **2. Statistical Modeling:**
   - Applied **ARIMA** (AutoRegressive Integrated Moving Average) for initial **statistical time series forecasting**, providing a baseline model.

### **3. Deep Learning Model:**
   - Implemented **deep learning models** using **LSTM** and **GRU** layers, designed to capture temporal dependencies in the time series data.
   - **LSTM with GRU Layer**: Two **LSTM layers**, one **GRU layer**, one **dropout layer**, and a **dense output layer** were used.
   - Optimized the model using **Adam optimizer** with **ReLU** activation function.

### **4. Evaluation Metrics:**
   - The model's performance was evaluated using **MAPE (Mean Absolute Percentage Error)**.
   - **Final model** achieved **MAPE** of **0.35 for CO** and **0.16 for temperature**, demonstrating robust accuracy.

---

## **Technologies Used**

- **Programming Language**: **Python**
- **Libraries**:
  - **ARIMA**: For **statistical modeling** of time series.
  - **TensorFlow**: **Deep learning framework** for building and training models.
  - **Keras**: **High-level API** for neural networks.
  - **scikit-learn**: For **data preprocessing**, model evaluation, and optimization.
  - **NumPy** & **Pandas**: For **data manipulation** and handling.
  - **Matplotlib**: For **data visualization**.

---

## **Model Performance**

| **Model Architecture**      | **CO (MAPE)** | **Temperature (MAPE)** |
|-----------------------------|---------------|------------------------|
| **LSTM with GRU Layer**      | **0.35**      | **0.16**               |
| **LSTM with Dense Layer**    | **0.35**      | **0.15**               |
| **LSTM with Conv1D Layer**   | **0.35**      | **0.24**               |

**Best Model:** **LSTM with GRU Layer**  
**Achieved MAPE:**  
- **CO:** **0.35**  
- **Temperature:** **0.16**

---

## **Results and Graphs**

### **Results Overview**

- **MAPE for CO**: **0.35**
- **MAPE for Temperature**: **0.16**
- The final model achieved a **MAPE** of **0.35 for CO** and **0.16 for temperature**, indicating high forecasting accuracy.

### **Day-wise Predictions:**

| **Day** | **CO(GT) MAPE** | **Temperature MAPE** |
|---------|-----------------|----------------------|
| **Day 8** | 0.18583         | 0.07434              |
| **Day 9** | 0.16049         | 0.27813              |
| **Day 10** | 0.47705        | 0.12950              |
| **Day 11** | 0.30354        | 0.06220              |
| **Day 12** | 0.63927        | 0.09712              |
| **Day 13** | 0.36005        | 0.39956              |
| **Day 14** | 0.29879        | 0.13799              |

### **Average MAPE:**

- **CO(GT) MAPE**: **0.34643**
- **Temperature MAPE**: **0.16841**

### **Graph of Predicted vs Actual Temperature**
<img width="785" height="413" alt="temp" src="https://github.com/user-attachments/assets/8b9cee95-6bf2-4c71-b1c1-d9fb1fde63fa" />

