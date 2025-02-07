# Sentiment-Analysis-in-Pharmaceutical-Industry

Cristiane Mecca Giacomazzi (Data Analyst)

This project was developed with Cross-industry standard process for data mining (CRISP-DM) methodology.

The following topics will be presented:

1. Business Understanding
2. Data Understanding
3. Ethical Statements
4. Data Preparation
5. Libraries used for this project
6. Project Plan
7. Metrics
8. Results
9. Communication and Action
10. References

**1. Business Understanding**

Sentiment Analysis (SA), a key area of Natural Language Processing (NLP), plays a vital role in interpreting the emotional tone of textual data. It involves examining large amounts of text to assess whether the sentiment is positive, negative, or neutral. SA tools are increasingly used by companies to filter reviews and Net Promoter Scores (NPS), removing personal bias and providing more objective insights into their brand, products, and services. The pharmaceutical industry is no exception, as SA is revolutionizing how companies analyze public sentiment and conversations about their products, becoming a central element of their digital strategy. 

This issue is particularly critical in healthcare, where understanding patient experiences and perceptions is essential. Given the growing importance of mining social media for insights, this project focuses on leveraging SA techniques to detect positive, negative, and neutral opinions surrounding the pharmaceutical industry. Using a publicly available dataset, the goal of this project is to analyze the data and identify the top 10 drugs with the most negative patient evaluations.

**2. Data Understanding**

Dataset Description: This dataset focuses on sentiment analysis in the healthcare domain. It contains patient reviews on specific drugs and related conditions and a 10-star patient rating reflecting overall patient satisfaction.

Features:

<img width="640" alt="Screen Shot 2024-12-09 at 3 05 19 PM" src="https://github.com/user-attachments/assets/aa90d497-6ea4-46c7-b1dd-2292bb843c99">

Table by author

**3. Ethical Statements**

For this project, it was used a public dataset from [UC Irvine Machine Learning Repository](https://archive.ics.uci.edu/dataset/462/drug+review+dataset+drugs+com).

**4. Data Preparation**

- Dataset Fetching: Retrieved data using fetch_ucirepo from the ucimlrepo module.

- Data Inspection: Checked the metadata and variables to understand the structure using print(drug_reviews_drugs_com.metadata) and print(drug_reviews_drugs_com.variables).

- Data cleaning: converting text to lowercase, removing punctuations and stopwords, in tokenizing.

- Tuning the model: to optimizer the hyperparameter tuning and improve the model's performance through Logistic Regression. Achieve the right balance between fitting the training data well (without overfitting) and generalizing well to new data. The features (X) and targets (y) were merged into a single DataFrame using pd.concat([X, y], axis=1). This creates a combined DataFrame (df) that can be processed further for sentiment analysis.

- Handling Missing Data: Checked for missing values in reviews and assigned a default sentiment ("Neutral") where necessary using pd.notnull(review)

- Sentiment Labeling: Applied sentiment analysis with TextBlob and VADER.

-- TextBlob Sentiment: The polarity score is used to classify the sentiment as "Positive", "Negative", or "Neutral".

-- VADER Sentiment: The compound score is used to classify the sentiment similarly based on predefined thresholds (> 0.05 for positive, < -0.05 for negative, and between for neutral).

- The sentiment results from both analyzers (TextBlob_Sentiment and VADER_Sentiment) are added as new columns in the DataFrame (df). This allows you to analyze the sentiment for each review side by side.

- Data Saving: Saved the enriched DataFrame to a CSV for later use.

**5. Libraries used for this project**

<img width="643" alt="Screen Shot 2024-12-09 at 3 08 56 PM" src="https://github.com/user-attachments/assets/27893e20-411b-4b2a-9ace-3b987740a6f3">

Table by author

**6. Project Plan**

<img width="666" alt="Screen Shot 2024-12-09 at 3 09 26 PM" src="https://github.com/user-attachments/assets/4c3c6b72-9aab-4ee7-8826-f15a98b09736">

Image by author

**7. Metrics**

Accuracy: 91.03%

Precision: 0.91

Recall: 0.91

F1-Score: 0.90

_Confusion Matrix_

<img width="533" alt="Screen Shot 2024-12-09 at 3 15 47 PM" src="https://github.com/user-attachments/assets/6238d084-3b8e-448c-b473-1062f9bfc44b">

Image by author


**8. Results**

<img width="929" alt="Screen Shot 2024-12-09 at 3 17 05 PM" src="https://github.com/user-attachments/assets/f10464d4-ce83-44b5-b7a1-36c756cd9b7b">


**9. Communication and Action****

<img width="633" alt="Screen Shot 2024-12-09 at 3 12 30 PM" src="https://github.com/user-attachments/assets/f2bbc9ac-f81f-43cd-add5-8afe1c4fd739">


Image by the author

**10. Referencecs**

Kallumadi, S. & Grer, F. (2018). Drug Reviews (Drugs.com) [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5SK5S

Korkontzelos, I., Nikfarjam, A., Shardlow, M., Sarker, A., Ananiadou, S., & Gonzalez, G. H. (2016). Analysis of the effect of sentiment analysis on extracting adverse drug reactions from tweets and forum posts. Journal of Biomedical Informatics, 62, 148–158. https://doi.org/10.1016/j.jbi.2016.06.007 

IBM. (n. d.). What is Sentiment Analysis? https://www.ibm.com/topics/sentiment-analysis 

Grissette, H., Nfaoui, E. H., Bahir, A. (2017). Sentiment Analysis tool for Pharmaceutical Industry & Healthcare. TMLAI, 5, 746-760.
http://dx.doi.org/10.14738/tmlai.54.3339 

Jadhav, S., Shiragapur, B., Purohit, R.,  Jha, N.(). A Systematic Review on the Role of Sentiment Analysis in Healthcare. Advance. 01, 2024.
http://dx.doi.org/10.22541/au.172516418.81416769/v1 









