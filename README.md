# SENTIMENT ANALYSIS :GOOGLE AND APPLE
[Presentation link](https://docs.google.com/presentation/d/16Fm9dSCugHTrsbJ6nj0aO-Sj6K0x0z2g9UWyxks_eVI/edit?usp=sharing)
## Business understanding

Google and Apple are multinational techonology companies well known for their products such as google sheets (from Google) and iPhone (from Apple).The companies have come up with ways to get their customer feedback such as,in app user feedback and rating, getting the tweets from Twitter(now X),among many others. However,since the companies are multinational it can be really difficult and tiresome to read through the millions of feedback or tweets from multiple apps in order to get the customers' view or sentiment about a product.As a result,the companies want to build a model that can rate the sentiment of a tweet or text based on its content.This will enable the companies to make improvements on their products or services to improve customer satisfaction and even attract more customers.

## Data understanding

The data used in this project was extracted from [data.world](https://data.world/crowdflower/brands-and-product-emotions). It contains tweets related to Google and Apple products which were ranked as negative,positive or neutral. This dataset contains over 9000 tweets.In addition to the tweets and their ratings,the dataset contains a column that shows the product the tweet is directed to.This dataset will be of great help when building a model for our sentiment analysis.

### Data preparation

In order to prepare the data for modelling various preprocessing steps were applied.These include:
- Dealing with missing values : 
    - One column had to be dropped due to a high number of missing cases.
- Renaming columns to have shorter column names.
- Reducing the categories in the emotion (renamed) column to only three.
- Word tokenization using nltk.
- Converting the labels to integers.
- Splitting the dataset.
- Word vectorization using CountVectorizer and TfidfVectorizer.

### Modelling

Four models were developed in this project as follows:
- Decision tree classifier using the outputs of the CountVectorizer.This was the baseline model.
- Decision tree classifier using the outputs of the TfidfVectorizer.
- Recurrent Neural Network model.This was the model with the highest accuracy.
- Random Forest Classifier model using the outputs of the TfidfVectorizer.

### Evaluation

Evaluation was done on the RNN model which had the highest accuracy compared to the other models (69% accuracy).It proved to be a good model since it had an accuracy score of 67% on the test set.The model can therefore generalize into unseen data.