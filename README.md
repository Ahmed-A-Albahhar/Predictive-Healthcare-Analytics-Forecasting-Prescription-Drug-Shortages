# Predictive-Healthcare-Analytics-Forecasting-Prescription-Drug-Shortages
📌 Project Overview
Frequent drug shortages severely disrupt patient care, increase operational costs, and force reliance on alternative medications that can introduce unaccounted side effects. This project focuses on the healthcare industry's supply chain, utilizing historical prescription data to build a predictive model that forecasts drug shortages in advance.
While the analytical framework is applicable to various medications, this case study specifically targets diabetes and weight-management medications, with a primary focus on Ozempic (semaglutide).   

🎯 Objectives
Demand Prediction: Develop a time-series forecasting model (ARIMA, SARIMA, Prophet) to predict shortages before they occur.   Trend Analysis: Visualize supply-demand trends and compare Ozempic shortage patterns against other diabetic medications.   Sentiment Analysis: Apply opinion mining to patient reviews to understand the real-world emotional and health impacts of these shortages.   

🗄️ Data Architecture
The project triangulates data from three primary sources to connect supply chain metrics with patient sentiment:   
- NHS Prescription Services (File 1): Historical drug usage patterns, tracking prescribed and dispensed frequencies (e.g., 0.25mg, 0.5mg, 1mg pens) from January 2019 to August 2023.
- Australian Government DHAC (File 2): Shortage event reports detailing supply impact dates, shortage impact ratings (Low, Medium, Critical), and root causes (e.g., manufacturing issues, demand spikes).
- WebMD Patient Reviews (File 3): Structured ratings (effectiveness, ease of use, satisfaction) and unstructured raw text for Natural Language Processing (NLP).
   
⚙️ Methodology (DCOVA Framework)
Define: Framed the operational problem and defined the forecasting goals.   
Collect: Gathered multi-source historical, categorical, and qualitative data.   
Organize: Handled missing values and engineered time-based features.   
Visualize: Conducted Exploratory Data Analysis (EDA) to map trends in items dispensed versus total quantity dispensed over time.   
Analyze:
- Implemented ARIMA, SARIMA, and Prophet time-series models.
- Conducted Analysis of Variance (ANOVA) to detect patterns across medication categories.
- Executed Sentiment Analysis on patient text data to correlate tone with shortage periods.
     
📊 Model Evaluation & Results
The models were evaluated using Root Mean Square Error (RMSE) and Mean Absolute Error (MAE) to determine the most accurate forecasting tool:      

  Model   |  RMSE   |  MAE    |
  
  ARIMA   |   8.8   |  5.8    |
  
  Prophet |  20.5   |  15.3   |
  
  SARIMA  |  36.99  |  25.59  |
  
Conclusion: The standard ARIMA model significantly outperformed the others in predicting medication dispensation quantities.   

🚀 Future Work & Strategic Recommendations
- Supply vs. Demand Buffering: Utilize model outputs for sophisticated inventory buffering to prepare for anticipated fluctuations.
- Advanced Feature Engineering: Incorporate detailed variables such as the exact length of shortage periods and fluctuation counts.
- Alternative Algorithms: Experiment with Exponential Smoothing, Moving Averages, and Naive Bayes.   
