# HAR-Model-Comparison-Deep-Learning-vs.-Machine-Learning
# Deep Learning vs. Machine Learning - Model Comparison

## Overview
This project compares Deep Learning models (LSTM and CNN-LSTM) with Machine Learning models (Random Forest, SVM, Logistic Regression) for time-series classification.

## Deep Learning Models

### 1. Data Preparation
- Raw time-series data with **128 time steps** and **6 sensor features**.

### 2. Training LSTM & CNN-LSTM Models
- **Hyperparameters:**
  - Epochs: **50**
  - Learning Rate: **0.001**

#### LSTM Model Summary:
- **First LSTM Layer**:
  - Parameters: `18,176`
- **Second LSTM Layer**:
  - Parameters: `12,416`
- **Dense Layer**:
  - Parameters: `198`
- **Total Parameters:** `30,790`

#### CNN-LSTM Model Summary:
- **Total Parameters:** `15,910`

### 3. Model Evaluation
- Metrics: **Accuracy, Precision, Recall, F1-Score**
- Classification reports generated for both models.

## Machine Learning Models

### 1. Data Preparation
- Uses handcrafted features like **Mean** and **Variance**.

### 2. Training Models
- Models: **Random Forest, SVM, Logistic Regression**

### 3. Model Evaluation
- Metrics: **Accuracy, Precision, Recall, F1-Score**
- Confusion matrix analyzed.

## Model Comparison
### Strengths & Weaknesses
| Model | Strengths | Weaknesses |
|--------|-----------------------------------|--------------------------------------|
| LSTM | Captures temporal dependencies well | Struggles with similar classes (Sitting vs. Standing) |
| CNN-LSTM | Captures both spatial & temporal patterns, outperforms LSTM | Computationally expensive |
| ML Models | Faster training, competitive performance | Relies on handcrafted features, may not capture complex patterns |

### Training Efficiency
- **Deep Learning Models:** Computationally expensive (**50 epochs**) but achieved higher accuracy.
- **Machine Learning Models:** Faster training (**10 epochs**) but less accurate.

### Class-Specific Performance
- **"Sitting" & "Standing"**: All models struggled due to similarity in motion patterns.
- **"Laying"**: Perfectly classified by all models.

## Visualizations
- **Bar Graph Representation** of Deep Learning vs. Machine Learning models.

## How to Run the Project
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the training script:
   ```bash
   python train.py
   ```
3. Evaluate model performance:
   ```bash
   python evaluate.py
   ```

## Contributors
- **[SHRI MONESH V]**


## License
This project is licensed under the MIT License.
