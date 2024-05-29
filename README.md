<a name="readme-top"></a>

<div align="center">
   <h1><b>Time-Series-Regression-Analysis : Predicting store sales for Corporation Favorita</b></h1>
</div>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

![image](https://github.com/MoIdris/Time-Series-Regression-Analysis/blob/LP3/Dashboard/image.png)

![image](https://github.com/MoIdris/Time-Series-Regression-Analysis/blob/LP3/Dashboard/Screenshot%202024-05-29%20000402.png)

Below is a summary of the procedure structure on this project. To view a full project documentation, kindly visit this page (https://medium.com/@idmoh44/machine-learning-model-time-series-regression-analysis-fccf3dda5f59)

<!-- TABLE OF CONTENTS -->

# 📗 Table of Contents

- [📗 Table of Contents](#-table-of-contents)
- [Introduction ](#introduction-)
  - [🛠 Built With ](#-built-with-)
    - [Tech Stack ](#tech-stack-)
  - [Key Features ](#key-features-)
  - [💻 Getting Started ](#-getting-started-)
    - [Prerequisites](#prerequisites)
    - [Setup](#setup)
    - [Install](#install)
    - [Usage](#usage)
  - [👥 Authors ](#-authors-)
  - [🔭 Future Features ](#-future-features-)
  - [🤝 Contributing ](#-contributing-)
  - [⭐️ Show your support ](#️-show-your-support-)
  - [🙏 Acknowledgments ](#-acknowledgments-)
  - [📝 License ](#-license-)

<!-- PROJECT DESCRIPTION -->

# Introduction <a name="about-project"></a>
The primary objective of Corporation Favorita’s data analysis initiative should be to develop a predictive model that can accurately forecast the unit sales of its products. This model aims to:

Analyze historical sales data to identify trends and patterns in consumer demand.
Predict future product demand with a high degree of accuracy using advanced machine learning techniques.
Inform purchasing and stocking decisions to optimize inventory levels, avoiding both stockouts and overstocking.
Enhance operational efficiency by aligning product availability with anticipated market demand.
Improve customer satisfaction by ensuring that popular items are in stock when and where they are needed.
By achieving these objectives, Corporation Favorita can maintain its competitive edge in the retail market and continue to meet the evolving needs of its customers.

### Project Plan: 

The project plan involves several steps. First, the data will be prepared for analysis, which may include cleaning the data, handling missing values, and encoding categorical variables. Next, appropriate machine learning algorithms will be selected for model construction.

By aligning these steps with the overall business strategy, the company can ensure a data-driven approach to predict unit sales of items for different stores, ultimately leading to business growth and customer satisfaction.

Key Stakeholders

Stakeholders include Corporation Favorita’s management, sales and marketing teams, store managers, and data science team.

Analytical Goals

- Handle missing values in the datasets by imputation techniques such as mean, median, or mode.

- Address outliers in sales data that may skew the model’s predictions by applying robust statistical methods or trimming techniques.

- Normalize or scale numerical features to ensure uniformity and improve model performance.

- Encode categorical variables using techniques such as one-hot encoding or label encoding.

- Build time series regression models such as SARIMA, ARIMA, XGBoost, Linear Regression etc. to capture seasonality and trends in sales data.

- Validate models using cross-validation techniques and assess their performance metrics such as RMSE (Root Mean Squared Error) or MAE (Mean Absolute Error).

- Create insightful visualizations and dashboards for sales analysis and forecasting.

Success Criteria

- Achieve a 0.2 RMSE (Root Mean Squared Error) in sales forecasting models.

- Improve inventory management efficiency and reduce stockout instances.

Constraints and Assumptions

- Assumption: Historical sales data is representative of future demand patterns.

Constraint: Limited availability of real-time sales data for model training.

Data Requirements

- Utilize data from train.csv, stores.csv, holidays_events.csv, oil.csv, and transaction.csv for analysis.

- Include features such as store_nbr, family, onpromotion, store metadata, oil prices, holidays, and transactional data.

Business Impact

- Enhance customer satisfaction through better product availability.

- Optimize inventory management, leading to cost savings and improved operational efficiency.

### Data for the Project:

The data for this project has been divided into 2. The first data set are for training and evaluation the machine learning model while the last data set is for testing the model.

The training dataset can be found in a database which will have to be accessed remotely and a zip file hosted on Github repository.

The test dataset for this project can be found in OneDrive.

File Descriptions and Data Field Information

**train.csv**

- The training data, comprising time series of features store_nbr, family, and onpromotion as well as the target sales.

- store_nbr identifies the store at which the products are sold.

- family identifies the type of product sold.

- sales gives the total sales for a product family at a particular store at a given date. Fractional values are possible since products can be sold in fractional units (1.5 kg of cheese, for instance, as opposed to 1 bag of chips).

- onpromotion gives the total number of items in a product family that were being promoted at a store at a given date.

**test.csv**

- The test data, having the same features as the training data. You will predict the target sales for the dates in this file.

- The dates in the test data are for the 15 days after the last date in the training data.

**transaction.csv**

- Contains date, store_nbr and transaction made on that specific date.

**sample_submission.csv**

- A sample submission file in the correct format.

**stores.csv**

- Store metadata, including city, state, type, and cluster.

- cluster is a grouping of similar stores.

**oil.csv**

- Daily oil price which includes values during both the train and test data timeframes. (Ecuador is an oil-dependent country and its economical health is highly vulnerable to shocks in oil prices.)

**holidays_events.csv**

- Holidays and Events, with metadata

**NOTE:** Pay special attention to the transferred column. A holiday that is transferred officially falls on that calendar day but was moved to another date by the government. A transferred day is more like a normal day than a holiday. To find the day that it was celebrated, look for the corresponding row where type is Transfer.

For example, the holiday Independencia de Guayaquil was transferred from 2012–10–09 to 2012–10–12, which means it was celebrated on 2012–10–12. Days that are type Bridge are extra days that are added to a holiday (e.g., to extend the break across a long weekend). These are frequently made up by the type Work Day which is a day not normally scheduled for work (e.g., Saturday) that is meant to payback the Bridge.

Additional holidays are days added a regular calendar holiday, for example, as typically happens around Christmas (making Christmas Eve a holiday).

Additional Notes

Wages in the public sector are paid every two weeks on the 15th and on the last day of the month. Supermarket sales could be affected by this.

A magnitude 7.8 earthquake struck Ecuador on April 16, 2016. People rallied in relief efforts donating water and other first need products which greatly affected supermarket sales for several weeks after the earthquake.

## 🛠 Built With <a name="built-with"></a>

### Tech Stack <a name="tech-stack"></a>

<details>
<summary>Database</summary>
  <ul>
    <li><a href="">Microsoft SQL Server</a></li>
  </ul>
</details>

<details>
<summary>Language</summary>
  <ul>
    <li><a href="">Python</a></li>
    <li><a href="">Jupyter Notebook</a></li>
  </ul>
</details>

<details>
<summary>Model</summary>
  <ul>
    <li><a href="">Sklearn</a></li>
  </ul>
</details>


<p align="right">(<a href="#readme-top">back to top</a>)</p>
<!-- Features -->

## Key Features <a name="key-features"></a>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

**1. Business Understanding:**
This is the initial phase where I define the business problem, objectives, and outcomes. I also identified the key stakeholders and understand their expectations.

**2. Data Understanding:**
This phase involves the following steps:

- Importation: Acquiring the necessary data for the project.
- Data Loading: Loading the data into a suitable format for analysis.
- Action Plan: Creating a plan for how to approach the data analysis.
- Hypothesis: Formulating hypotheses that I will test during the analysis.
- Business Questions: Identifying the key questions that the business needs answers to.

**3. Data Preprocessing:**
This phase involves preparing the data for analysis. This could include data cleaning, data transformation, and data integration.

**4. Data Cleaning:**
This phase involves identifying and correcting errors in the data, dealing with missing values, and removing duplicates.

**5. Hypothesis Testing:**
This phase involves testing the hypotheses that were formulated during the data understanding phase. This could involve statistical tests to determine if there is a significant relationship between variables.

**6. Exploratory Data Analysis (EDA):**
This phase involves exploring the data to understand its characteristics and patterns. This could involve visualizing the data, calculating descriptive statistics, and identifying correlations.

**7. Analysis of Business Questions:**
This phase involves using the insights gained from the EDA and hypothesis testing to answer the business questions identified earlier. This could involve building predictive trends, segmenting the data, or conducting further statistical tests.

<!-- GETTING STARTED -->

## 💻 Getting Started <a name="getting-started"></a>


To get a local copy up and running, follow these steps.

### Prerequisites

In order to run this project you need:

- Python


### Setup

Clone this repository to your desired folder:


```sh
  cd my-folder
  git clone https://github.com/MoIdris/Time-Series-Regression-Analysis.git
```

Change into the cloned repository

```sh
  cd Time-Series-Regression-Analysis
  
```

Create a virtual environment

```sh

python -m venv env

```

Activate the virtual environment

```sh
    env/Scripts/activate
```

### Install

Here, you need to recursively install all the necessary packages to be imported in your notebook 

```sh
   pip install python-dotenv
   pip install pyodbc
   pip install numpy
   pip install pandas
   pip install seaborn
   pip install scipy
   pip install jupyterlab
```


### Usage

To view this analysis, visit the page (https://github.com/MoIdris/Time-Series-Regression-Analysis.git)

To download the notebook, execute the following steps:


- Navigate to the GitHub page (https://github.com/MoIdris/Time-Series-Regression-Analysis.git).
- Click on the notebook file name to open it.
- Once the file is open, you will see a Raw button on the top right of the file content. Click on this Raw button.
- The notebook content will be displayed in raw JSON format. Right-click anywhere on the page and select Save As or press Ctrl+S to save the file.
- In the Save dialog box, make sure to add the .ipynb extension to the file name if it’s not already there. For example, if the file name is notebook, change it to notebook.ipynb.
- Choose the location where you want to save the file and click Save.
- Now, you can open this .ipynb file using Jupyter Notebook on your local machine.
- **Please note** that the file might be saved as a .txt file by default, so ensure that you change the extension to .ipynb when saving

## Data Cleaning

The data used in this analysis was sourced from three different sources, github, sql server and onedrive, a connection was created with a connection string defined in the '.env' file

1. Data Collection: Gathering raw data from online database.

2. Data Integration: Consolidating data from different sources into a unified dataset.

3. Missing Value Handling: Identifying and dealing with missing values through imputation or removal.

4. Outlier Detection: Detecting and handling outliers that could skew the analysis results.

5. Normalization and Standardization: Ensuring consistency and comparability of data by normalizing or standardizing where necessary.

6. Data Validation: Verifying the integrity of the cleaned dataset to ensure accuracy in subsequent analyses.

## Data Representation

The cleaned data was represented in structured formats suitable for analysis. This included organizing data into tables and saving the unified dataset as a single '.csv' file. Visualization techniques such as charts, graphs, and maps were also employed to present key findings effectively.

## Analysis Methods

Various analytical methods and techniques were utilized to extract insights from the data:

1. Descriptive Statistics: Summarizing key metrics such as mean, median, mode, and standard deviation to describe the central tendency and dispersion of variables.
2. Time-Series Analysis: Examining trends and patterns over time to understand the evolution of the startup ecosystem.
3. Correlation Analysis: Investigating relationships between different variables, such as funding amount and startup success rate.
4. Segmentation Analysis: Grouping startups based on common characteristics (e.g., sector, funding stage) and analyzing each segment separately.
5. Predictive Modeling: Building predictive models to forecast future trends or identify factors influencing startup performance.

## Final Findings

Based on the analysis conducted, several key findings emerged:

- Incorporate the SARIMA model into Corporation Favorita's forecasting framework to enhance the accuracy and reliability of sales predictions.

- Regularly monitor model performance and refine forecasting methodologies to adapt to evolving market dynamics and consumer behavior.

- Consider exploring hybrid models that combine the strengths of SARIMA, ARIMA, and Prophet models to further improve forecasting accuracy.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

![image](https://github.com/MoIdris/Time-Series-Regression-Analysis/blob/LP3/Dashboard/Screenshot%202024-05-29%20002319.png)


<!-- AUTHORS -->

## 👥 Authors <a name="authors"></a>

🕵🏽‍♀️ **Mohammed Idris**

- GitHub: [GitHub Profile](https://github.com/MoIdris)
- Twitter: [Twitter Handle](https://twitter.com/IdrisBaaba)
- LinkedIn: [LinkedIn Profile](www.linkedin.com/in/idris-ibn-mohammed)
- Medium: [Medium Profile](https://medium.com/@idmoh44)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- FUTURE FEATURES -->

## 🔭 Future Features <a name="future-features"></a>


- **Add a front end application for users**
  
  
<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## 🤝 Contributing <a name="contributing"></a>

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- SUPPORT -->

## ⭐️ Show your support <a name="support"></a>

If you like this project kindly show some love, give it a 🌟 **STAR** 🌟

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGEMENTS -->

## 🙏 Acknowledgments <a name="acknowledgements"></a>

I would like to thank all my team member for their coorperation, commitment and support. My greatest appreciation goes to Rahael for their immense guidance and support.Thanks to all online contributors for the available resources.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->

## 📝 License <a name="license"></a>

This project is [MIT](./LICENSE) licensed.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
