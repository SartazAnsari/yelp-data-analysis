# Yelp Dataset Analysis

## Overview
This project involves analyzing the Yelp dataset to understand the characteristics of businesses, user interactions, and trends within the Yelp community. The dataset includes information on businesses, user reviews, check-ins, tips, and user data. This project provides two methods for performing analysis.
1. **Analysis on Kaggle Notebook:**
    * In this method, you perform the analysis directly on Kaggle using only Python.
    * You can add the dataset from Kaggle to the notebook without needing to download it to your local system.
2. **Analysis on Local System Analysis with MySQL:**
    * In this method, you download the dataset to your local system and create a MySQL database.
    * The data is uploaded into the MySQL database, and analysis is performed using a combination of Python and SQL.

***Note:** The original dataset is provided by [Yelp, Inc.](https://www.kaggle.com/organizations/yelp-dataset) in Kaggle and can be found [here](https://www.kaggle.com/datasets/yelp-dataset/yelp-dataset). Credit goes to the dataset provider for making it available.*

## Viewing the Notebook
For better readability due to custom client display functionality, use [nbviewer](https://nbviewer.org). This provides an improved display as GitHub's notebook viewer does not execute the code.
1. [YelpDataAnalysis.ipynb](https://nbviewer.org/github/SartazAnsari/yelp-data-analysis/blob/main/YelpDataAnalysis.ipynb)
2. [YelpDataAnalysis(Kaggle).ipynb](https://nbviewer.org/github/SartazAnsari/yelp-data-analysis/blob/main/YelpDataAnalysis(Kaggle).ipynb)

## Method 1: Analysis on Kaggle Notebook

1. **Login to Kaggle:** Go to Kaggle and log in to your account. If you don't have an account, create one.
2. **Create a New Notebook:** On the Kaggle homepage, click on `Create` > `New Notebook`
3. **Import the Notebook from GitHub:** In the notebook, click `File` > `Import notebook` > `Github` and paste [this link](https://github.com/SartazAnsari/yelp-data-analysis/blob/main/YelpDataAnalysis(Kaggle).ipynb) and click `import`.
4. **[ If not added ] Add the Yelp Dataset:** In the notebook, click on `File` > `Add Input` and paste [this link](https://www.kaggle.com/datasets/yelp-dataset/yelp-dataset) on the right-hand side search and click on the result (Yelp Dataset).

## Method 2: Analysis on Local System Analysis with MySQL

### Prerequisites
1. **Python 3.x:** Download and install from [python.org](https://www.python.org/).
2. **MySQL Server:** Download and install from [mysql.com](https://dev.mysql.com/downloads/mysql/).

### Setup
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/SartazAnsari/yelp-data-analysis.git
   cd yelp-data-analysis
   ```

2. **Environment setup**
    * Using **Python**
        1. Create virtual environment: 
            ```bash
            python -m yelp-data-analysis-env
            ```
        2. Activate the environment:
            * Windows: 
                ```bash
                yelp-data-analysis-env\Scripts\activate
                ```
            * Unix or MacOS:
                ```bash
                source yelp-data-analysis-env/bin/activate

                ```
        3. Install the required packages:
            ```bash
            pip install notebook
            pip install ipykernel
            pip install kaggle
            pip install pandas matplotlib seaborn mysql-connector-python sqlalchemy psutil
            ```
    * Using **Conda**
        1. Install **Miniconda/Anaconda**: Download and install from [conda.io](https://conda.io).
        2. Create a new environment:
            ```bash
            conda create --name yelp-data-analysis-env python=3.12
            ```
        3. Activate the environment:
            ```bash
            conda activate yelp-data-analysis-env
            ```
        4. Install the required packages:
            ```bash
            conda install -c conda-forge notebook
            conda install -c conda-forge ipykernel
            conda install -c conda-forge kaggle
            conda install pandas matplotlib seaborn mysql-connector-python sqlalchemy psutil
            ```

3. **[ IF NOT SET BEFORE ] Setting up the Kaggle API**
    * Sign in to **Kaggle** and navigate to the **Account** tab of your user profile.
    * Scroll down to the **API** section and click on **Create New API Token**. 
    * This will download a file named ```kaggle.json``` containing your API credentials.
    * Place the ```kaggle.json``` file in the ```~/.kaggle/``` directory. If the directory does not exist, create it.
    * You're all set up! You can now use the Kaggle API to download datasets directly to your project.

## Analysis
1. **Data Overview:** Loaded tables, counted businesses, identified restaurant counts, and open statuses.
2. **Descriptive Stats:** Analyzed open restaurants for review_count and stars, and removed outliers.
3. **Top Restaurants:** Identified top 10 restaurants by review count and ratings, and highlighted top cities for restaurants.
4. **Engagement Metrics & Correlation:** Calculated and visualized reviews, tips, and check-ins. Analyzed relationships between these metrics.
5. **Categorization:** Compared high-rated and low-rated restaurant metrics.
6. **Trends Over Time:** Visualized review and tip trends.
7. **Sentiment Analysis:** Assessed useful, funny, and cool review metrics.
8. **User Contribution:** Compared elite vs. non-elite user reviews.

## Usage
1. Ensure the dataset is available in the project directory.
2. Import the necessary libraries and functions.
3. Run the provided Python script to perform the analysis and generate visualizations.