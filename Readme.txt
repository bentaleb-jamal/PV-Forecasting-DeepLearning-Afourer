                "Comparative Evaluation of Deep Learning Models for PV Power Forecasting
                Case Study: Afourer Hydropower Site, Morocco"

This repository contains the complete source code (10 Google Colab Notebooks) associated with the 
research article: "Comparative Evaluation of Deep Learning Models for Short-Term Photovoltaic Power 
Forecasting: Impact of Training Data Length and Application to the Afourer Hydropower Site (Morocco)"

📝 Project Overview

This study analyzes the impact of historical training data depth on the accuracy of short-term Photovoltaic
 (PV) power forecasting. To ensure full reproducibility, each deep learning architecture and study period (14 years vs. 5 years) 
has been isolated into separate notebooks.

📊 Data and Study Site

• Location: Afourer Hydropower Site, Morocco.
• Data Source: Hourly data extracted from PVGIS (Photovoltaic Geography Information System).
• Source File: Afourer_PVGIS_Data.csv (or the original PVGIS filename).
• Technical Note: The data loading scripts are configured to skip the first 10 metadata rows (skiprows=10).

📁 Project Structure (10 Notebooks)
The project is organized by model architecture and data depth:

14-Year Horizon (2010 - 2023)

• LSTM_14.ipynb: Long Short-Term Memory (Optimal Performance: R² = 0.9604)
• GRU_14.ipynb: Gated Recurrent Unit
• CNN_14.ipynb: Convolutional Neural Networks
• CNN_LSTM_14.ipynb: Hybrid CNN-LSTM Architecture
• CNN_GRU_14.ipynb: Hybrid CNN-GRU Architecture

5-Year Horizon (2019 - 2023)

• LSTM_5.ipynb: Impact study on reduced data depth
• GRU_5.ipynb: Robustness analysis on short-term cycles
• CNN_5.ipynb: Spatio-temporal performance analysis
• CNN_LSTM_5.ipynb: Sensitivity of hybrid models
• CNN_GRU_5.ipynb: Temporal consistency analysis

🛠️ Execution Instructions

1. Platform: Use Google Colab.
2. Hardware: Enable GPU Acceleration (Menu: Runtime > Change runtime type > Hardware accelerator: GPU).
3. Model Configuration:
o Input: 24-hour sliding window (t-23 to t).
o Output: Next-hour PV power prediction (t+1).
o Features (9): P, Gb(i), Gd(i), T2m, WS10m, hour_sin, hour_cos, month_sin, month_cos.
4. Setup: Upload the Afourer_PVGIS_Data.csv file to your Colab session before running the cells.

Key Dependencies:

• Python 3.x
• TensorFlow 2.x / Keras
• Pandas, Numpy, Scikit-learn, Matplotlib, Seaborn

🎓 Citation

Bentalab, J., al. "Comparative Evaluation of Deep Learning Models for Short-Term Photovoltaic 
Power Forecasting: Impact of Training Data Length and Application to the Afourer Hydropower Site (Morocco)"

📬 Contact

Jamal Bentalab - Faculty of Science and Technology (FST) Beni Mellal, Morocco. 
E-mail: bentalebj383@gmail.com

