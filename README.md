# ADS_599_Group-1-Capstone-Project

# Predicting Market Trends: Analyzing the Correlation Between SEC 8-K Disclosures and Stock Price Movements 

This project is part of the ADS_599 Capstone Project course in the Applied Data Science Program at the University of San Diego.

# -- Project Status: Completed

## Table of Contents
1. [Installation](#installation)
2. [Project Intro/Objective](#project-introobjective)
3. [Partner(s)/Contributor(s)](#partnerscontributors)
4. [Methods Used](#methods-used)
5. [Technologies](#technologies)
6. [Project Description](#project-description)
7. [Results and Findings](#results-and-findings)
8. [Conclusion](#conclusion)
9. [License](#license)
10. [Acknowledgments](#acknowledgments)

# Installation
1. Clone this repository:
git init
git clone https://github.com/DiprajBista/ADS_599_Group-1-Capstone-Project.git

2. Install the required Python libraries:
pip install -r requirements.txt

3. Download the SEC financial disclosures dataset (if not included) and store them in the appropriate folder.

4. You will also need to install spaCy’s English language model:
python -m spacy download en_core_web_sm

# Project Intro/Objective
The project is based on utilizing Natural Language Processing (NLP) and leveraging FinBERT for sentiment analysis of financial filings to predict stock price movements. The project aims to empower retail investors by providing insights from the company’s financial documents. Among various SEC filing financial documents to predict the market stock trend, the project adopts 8-K filings.  

# Partner(s)/Contributor(s)
1. Dip Raj Bista
2. Ghassan Seba 
3. Landon Padgett

# Methods Used
1. Data Preprocessing
2. Web Scraping
3. Data Visualization
4. Data Engineering
5. Predictive Modeling
6. Machine Learning
7. Text Mining
8. Sentiment Analysis with FinBERT
9. Topic Modeling

# Technologies
1. Python
2. FinBERT
3. Libraries: BeautifulSoup, Requests, spaCy, scikit-learn, NMF, LSA, LDA

# Project Description
The project is outlined in the following steps.

# Data Retrieval and Processing
# 1.	Retrieval:
Using Central Index Key (CIK) information, SEC filings are retrieved with the help of the unique custom function get_cik_number_by_ticker. To analyze the potential impact on the stock price movement, SEC documents 8-K filings are retrieved and stored. 8-K filing discloses significant company events such as mergers, acquisitions, etc. 

# 2.	Exploration: 
The raw retrieval data is organized in a structured format to continue further development and analysis. The several components of SEC filings are accession numbers, filing dates, document descriptions, etc. These steps laid the foundation for the further data processing process focusing on the 8-K filing. This helps to identify which data are substantial for stock prices. 

# 3.	Scraping: 
BeautifulSoup, a Python library, is implemented for scraping SEC 8-K filing from the EDGAR database. The scraping events focus on the events that influence stock price from the large corpus of datasets available. The scrapped volume of data needs to be processed later for sentiment analysis and correlation analysis with the market stock price.   

# 4.	Processing:
The scrapped SEC 8-K filing data is cleaned and processed for the  next steps. Data preprocessing includes removing irrelevant data, normalizing the data, and standardizing the data format. The FinBERT model requires the processed uniformly structured data for applying the sentiment analysis. This processing step is crucial as we prepare the dataset for extracting insights into the relationship between sentiment and stock market price fluctuations. 
  
# Modeling
The modeling section explores the relationship between sentiment extracted from the SEC 8-K filing and market stock fluctuations. The FinBERT model performs the financial sentiment analysis to predict market stock price using regression and classification. Some of the implemented regression algorithms are  Random Forest, Gradient Boosting Machines (GBMs), Neural Networks, and Support Vector Regressors (SVRs). The significant features of the data such as sentiment scores, prices, and stock volume are preprocessed to analyze class imbalance, feature scaling, and correlations. Model optimization is also tried with the exploration of hyperparameter tuning and SMOTE for classification.      

# Results and Findings 
The regression models such as Random Forest and Gradient Boosting struggled to predict the stock price movement because of the market noise and limited explanatory power of sentiment and financial features. Neural Networks and Support Vector regression models faced challenges in capturing significant relationships and produced inconsistent results. The performance of the gain/loss classification model achieved higher accuracy which could be explained because of the overfitting or class imbalance. The results and findings suggested that further research is required incorporating additional market variables as sentiment alone provided limited predictive power. 

# Conclusion
The project explores the sentiment analysis of the SEC 8-K filing using the FinBERT to uncover the correlations between the sentiment scores and stock price movement. The project aims to democratize the investment by providing financial insights to the retailer investors so that they can compete with institutional investors and make data-driven real-time investment decisions. The weak predictive performance of the regression model highlights the complexity of the financial market. The higher accuracy of the classification model is likely from the overfitting and class imbalance. The analysis confirms that sentiment analysis is a valuable technique but needs to be combined with macroeconomic variables, financial parameters, and collaborating with financial professionals. The project lays a solid foundation for future improvements. Future directions include incorporating more diverse datasets, and additional market variables, analyzing social media sentiment, enhancing predictive accuracies, and developing an interactive dashboard for broader access to financial insights.

# License
1. This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/licenses/MIT) file for details.
2. This project is licensed under the Apache License 2.0 - see the [LICENSE](https://www.apache.org/licenses/LICENSE-2.0) file for details.
3. This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](https://www.gnu.org/licenses/gpl-3.0.en.html) file for details.

# Acknowledgments

We would like to express our gratitude to the following individuals and organizations whose contributions and resources have been invaluable to the success of this project:

- **University of San Diego** for providing the academic foundation through the Applied Data Science Program.
- **Professor Ebrahim Tarshizi** for his guidance throughout the course.
- **FinBERT** for sentiment analysis of the financial text.
- **spaCy** for the Named Entity Recognition (NER) tool used in this project.
- **BeautifulSoup** and **Requests** libraries for web scraping functionality.
- **scikit-learn** and **NMF/LSA/LDA** libraries for the machine learning and topic modeling components.
- Open-source contributors who maintain the Python libraries crucial for this project.

