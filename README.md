# Vaccine passport hashtag prediction
As inoculations against COVID-19 continue across the country, fervent desires to return to normality  have intensified discussions of “vaccine passports”. Vaccine passport provides proof of vaccination for social activities that reduce public health restrictions for their bearers.  However, some use of passports to regulate access to social and recreational gatherings, workplaces, or schools appears to raise controversial discussions. Using passport to tailor restriction has drawn staunch opposition based on the concern that this practice can also be considered as discrimination to restrict the freedom of activities of those who have not yet get vaccinated. In order to explore crucial information from the discussion on vaccine passports, we focus on hashtags on Twitter.

Therefore, our goal is to identify the most accurate hashtag to a tweet related to covid vaccine passport and explore the crucial information from those tweets. Our solutions include two parts. Firstly, we would like to build models tTo identify the most accurate hashtag for a tweet’s content related to the vaccine passport. This can be done by building hashtag machine learning and deep learning with CountVectorizer and TfidfVectorizer and choosing the best model with the highest accuracy.  A good hashtag classifier could also benefit our second part of the solution, which aims to understand and explore the crucial information from tweets related to vaccine passports.  Secondly, we are curious how people look upon the covid vaccine passport topic and what topics under this discussion are considered the most important or widely discussed. Our approach contains WordCloud and topic modeling to find any crucial topic and keywords related to the tweet we collected

# Data sraping and cleaning
In the data_scraping.ipynb of data_scraping folder, we use Twint to crawl related data on these six hashtags: #vaccinepassport, #novaccinepassport, #greenpass, #nogreenpass, #vaccinemandate and #novaccinemandate from November 26 to December 5. Also, used “COVID” as the key word collected data from December 1 to December 5 with 20000 rows per day. The crawled raw data is stored at data folder including tagged_raw_data.csv, covid121.csv, covid122.csv, covid123.csv,c ovid124.csv, covid121.csv

In the data_preprocessing.ipynb of data_preprocessing, we conduct different precprocessing and cleaning techniques to handle raw data. The cleaned data cleaned_data.csv is storeed at data folder.

# Modeling
We build all models under the modeing folder.
In the DF_IDF_IDF.ipynb, we conduct experiments with baseline model, Multinominal NB, logistice regression, random forest, linear SVM and XGBoost with TF-IDF and Count vecterizor. After evaulation, we found that XGBoost with TF-IDF perform the best, then we save the model as xgb_tfidf.sav.
In the xgb_tfidf_otherfeatures.ipynb, we tried use more feataures to imporve the peformace of XGBoost.
For LSTM_model.ipynb, we train a deel learning model, LSTM

# Prediction and Analysis
In the vaccine_passport_hashtag_prediction folder,as Prediction_and_analysis_of_covid_related_tweet.ipynb, we predict all unlabeled covid data with our best model. Then analysis the covidvaccine-realted results by owrd cloud and topic modeling.  
