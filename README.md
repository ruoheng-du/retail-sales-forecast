# Time Series Forecasting of Retail Sales | Spring 2025
This is the repository for the Retail Sales Forecasting project completed for the Forecasting course during Spring 2025. The project focuses on predicting weekly overall retail sales by applying statistical, machine learning, and foundation time series models. The goal is to evaluate the accuracy and applicability of different forecasting techniques in a complex retail setting, supporting better inventory management and strategic planning.

The dataset is UCI Online Retail II, with over 1 million transactions from an online retailer. After cleaning, deduplication, and resampling, the target variable was defined as weekly total sales. Products were further grouped into two clusters via KMeans based on sales patterns to support cluster-specific forecasting.

<img width="500" alt="eda" src="https://github.com/ruoheng-du/retail-sales-forecast/raw/main/assets/eda.png">

<img width="500" alt="cluster" src="https://github.com/ruoheng-du/retail-sales-forecast/raw/main/assets/cluster.png">

This project experimented with four forecasting approaches:

- Facebook Prophet: Additive time series model that captures trend, seasonality, and holiday effects.

- Amazon Chronos: Pretrained foundation model for time series forecasting, tested in both zero-shot and fine-tuned modes using AutoGluon.

- XGBoost: Gradient boosting trees with engineered lag and calendar features to capture temporal dependencies.

- LightGBM: Efficient boosting model trained with time-based features and product-level grouping.

Forecasting accuracy was evaluated using Mean Absolute Percentage Error (MAPE). Prophet without clustering achieved the best performance with a MAPE of 10.65%. Chronos with zero-shot achieved a best MAPE of 14.27%. XGBoost achieved 17.97% after fine-tuning, while LightGBM achieved 18.03%. All models outperformed the previous baseline of 34.08%, showing strong improvements through improved preprocessing, feature engineering, and clustering.

Please feel free to contact me at ruoheng.du@columbia.edu for more information.

* This project is done in collaboration with Zhiqi Ma, Xiaojiang Wu, and Yijian Liu.
