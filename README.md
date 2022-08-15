# -Build-an-ML-system-for-forecasting-hourly-electricity-demand

Objective

With few exceptions, electricity must be generated at the same time it is needed. This creates a challenge for electrical grid operators who have to make a plan to generate the electricity their customers need each hour. Accurately forecasting energy demand is critical for grid operators so they can appropriately plan to meet the generation needs of their customers.

This project utilizes Data Engineering and Machine Learning Operations (MLOps) concepts to build a system for forecasting hourly electricity demand.

Data Engineering

I applied data engineering and EtLT concepts from the modern data stack including workflow orchestration with Airflow, cloud data warehousing and data lake storage on Google Cloud, and data transformation with dbt. I used these concepts and tools to build a data pipeline that populates a Big Query data warehouse with the data a data scientist needs to make develop an hourly day-ahead demand forecast.


![image](https://user-images.githubusercontent.com/96236642/184609614-ed4b537a-0cfa-454f-88a5-273cd2ced9ea.png)


MLOps

Once the data pipeline was running, I used concepts and tools from MLOps to build a system for developing, deploying, and monitoring machine learning models that predict hourly energy demand. I used experiment tracking and model registration with MLFlow, batch model deployment with Airflow, and model monitoring with dbt and Streamlit.


![image](https://user-images.githubusercontent.com/96236642/184609835-59b66c31-59fa-45a9-81d1-106ee98aac72.png)


High level requirements

The system should allow users to access historical electricity demand, EIA demand forecasts, historical weather data, and up-to-date weather forecast data in a Big Query data warehouse

The scope will be limited to the Public Service Company of Colorado Balancing Authority (aka Xcel Energy)

There should be an interactive dashboard to interact and visualize the data that is being loaded into the data warehouse

An MLFlow tracking server, artifact storage, and model registry should be used to track the models that are being developed and deployed

Production models should be deployed from the model registry to Airflow for batch model deployment

Model performance metrics should be tracked and visualized in a dashboard
Data Sources
Notebooks exploring each of these data sources can be found here

Electricity Demand and Generation - EIA Open Data

The United States Energy Information Administration (EIA) provides open access to hundreds of thousands of time series datasets via a REST API. The data is in the public domain, and requires registraton and an API key.

Historical Weather Data - NOAA Integrated Surface Data

The United States National Oceanic and Atmospheric Administration (NOAA) maintins the Integrated Surface Database (ISD) with global hourly weather station observations from nearly 30,000 stations. The data is available in csv format in open AWS S3 bucket.

Live weather data - Open Weather Map API

Live weather observation data for anywhere on the globe is available for free (with certain API call limits) via the Open Weather Map REST API.

Weather Forecast Data - NOAA National Digital Forecast Database

NOAA maintains the National Digital Forecast Database (NDFD) which is a suite of gridded forecasts of weather conditions for the United States. The data is available in gridded format in an open AWS S3 bucket or via XML from a REST API.

Technologies and Tools

Cloud - Google Cloud Platform

Infrastructure as Code - Terraform

Containerization - Docker and Docker Compose

Workflow Orchestration - Airflow

Pre-Load Transformation - pandas and pyarrow

Data Lake - Google Cloud Storage

Data Warehouse - BigQuery

Post-Load Transformation - dbt

Data Visualization/Dashboard - Streamlit and Plotly Express and hvplot

Model Development, Experiment Tracking, and Registration - scikit-learn and MLflow

Model Deployment - Batch Deployment with Airflow

Model Monitoring - dbt and Streamlit


Data and Forecast Dashboard


![image](https://user-images.githubusercontent.com/96236642/184610434-9dee0384-71fa-425d-8e64-b385a2eaecb7.png)


Note: I am running low on free GCP credits.



Monitoring Dashboard


![image](https://user-images.githubusercontent.com/96236642/184610513-7ae432c8-eaf3-425a-b6a4-1d3c3d721c00.png)


Data and Forecast Dashboard

