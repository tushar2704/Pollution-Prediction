# Pollution-Prediction



![Python](https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=Python&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Markdown](https://img.shields.io/badge/markdown-%23000000.svg?style=for-the-badge&logo=markdown&logoColor=white)
![Microsoft Office](https://img.shields.io/badge/Microsoft_Office-D83B01?style=for-the-badge&logo=microsoft-office&logoColor=white)
![Microsoft Word](https://img.shields.io/badge/Microsoft_Word-2B579A?style=for-the-badge&logo=microsoft-word&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Windows Terminal](https://img.shields.io/badge/Windows%20Terminal-%234D4D4D.svg?style=for-the-badge&logo=windows-terminal&logoColor=white)

## Problem Description

Air pollution is a critical environmental issue that poses significant health and well-being risks to individuals. Particulate Matter (PM) is a major air pollutant, with PM2.5 referring to fine particles measuring 2.5 micrometers or smaller that can deeply penetrate the respiratory system. Accurate forecasting of PM2.5 levels is essential for effective public health management, environmental planning, and policy-making. This project aims to develop machine learning models to forecast PM2.5 levels in the Jeongnim-Dong area from 2018 to 2022.
## Project Structure

The project repository is organized as follows:

```

├── LICENSE
├── README.md           <- README .
├── notebooks           <- Folder containing the final reports/results of this project.
│   │
│   └── pollution.py   <- Final notebook for the project.
├── reports            <- Folder containing the final reports/results of this project.
│   │
│   └── Report.pdf     <- Final analysis report in PDF.
│   
├── src                <- Source for this project.
│   │
│   └── data           <- Datasets used and collected for this project.
|   └── model          <- Model.

```

## Data and Data Preprocessing

The dataset comprises historical PM2.5 values for various cities. For this project, we filter the data to focus on the city of 'Jeongnim-Dong' and extract PM2.5 values within the specified timeframe (2018-2022). Preprocessing involves handling missing dates and ensuring a consistent daily data frequency. Any missing PM2.5 values are imputed using the preceding day's value, and the dataset is sorted chronologically by date.

## Data Visualization

We employ line plots to visualize the time series data depicting PM2.5 values in Jeongnim-Dong from 2018 to 2022. Furthermore, we partition the data into training and testing subsets based on timestamps. The training dataset encompasses values up to December 31, 2020, while the testing dataset covers the period from January 1, 2021, to January 1, 2022.

## Modeling

This project involves the implementation of two distinct machine learning models for forecasting PM2.5 values:

### CNN Model (Convolutional Neural Network)

The CNN Model utilizes Convolutional layers to extract patterns from the input sequence. The architecture encompasses two Conv1D layers with Rectified Linear Unit (ReLU) activation functions, followed by Global Average Pooling, Flatten, and Dense layers. The model is compiled using the Huber loss function, with the Adam optimizer and Mean Absolute Error (MAE) as the evaluation metric. Training spans 50 epochs, facilitated by a custom learning rate scheduler and a callback function designed to halt training upon reaching an MAE below 10.0.

### Mixed Model

The Mixed Model combines Convolutional and Bidirectional Long Short-Term Memory (LSTM) layers. Its structure parallels that of the CNN Model, with added Bidirectional LSTM layers to capture bidirectional temporal patterns. Similar to the CNN Model, the Mixed Model is compiled with the Huber loss function, Adam optimizer, and trained for 50 epochs, utilizing the same learning rate scheduler and custom callback.

## Forecasting

The trained models are employed to forecast PM2.5 values for the testing dataset. Data is windowed with a predetermined window size, and predictions are generated for each window. We compute MAE scores for both models to gauge their forecasting accuracy.

## Future Work

1. Experiment with varying window sizes to assess their impact on forecasting accuracy.
2. Explore alternative machine learning models, including Time Series models (e.g., ARIMA, SARIMA) and advanced deep learning models (e.g., GRU, Transformer).
3. Enhance forecasting accuracy by integrating additional environmental and weather-related features into the models.
4. Apply hyperparameter tuning techniques to optimize model performance.
5. Implement an ensemble approach that amalgamates multiple models for more robust predictions.
6. Scrutinize residuals to identify potential patterns or model shortcomings.
7. Deploy the most proficient model as an online forecasting service for real-time PM2.5 predictions.


## License

This project is licensed under the [MIT License](LICENSE).
## Author
- <ins><b>©2023 Tushar Aggarwal. All rights reserved</b></ins>
- <b>[LinkedIn](https://www.linkedin.com/in/tusharaggarwalinseec/)</b>
- <b>[Medium](https://medium.com/@tushar_aggarwal)</b> 
- <b>[Tushar-Aggarwal.com](https://www.tushar-aggarwal.com/)</b>
- <b>[New Kaggle](https://www.kaggle.com/tagg27)</b> 

## Contact me!
If you have any questions, suggestions, or just want to say hello, you can reach out to us at [Tushar Aggarwal](mailto:info@tushar-aggarwal.com). We would love to hear from you!