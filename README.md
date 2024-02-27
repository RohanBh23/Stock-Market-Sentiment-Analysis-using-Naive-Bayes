# Stock-Market-Sentiment-Analysis-using-Naive-Bayes
Stock market sentiment analysis on data scraped from popular social networking site

Social Networking sites are a good source for getting raw public sentiment regarding anything relevent, be it Politics, Entertainment, and Stock market as well. For this project, Reddit has been used to get relevent data regarding stock market.
(Visit- https://www.reddit.com/r/StockMarket/)


## OVERVIEW

Here's an overview of my project and the steps involved:

1. **Libraries Used**: Important Python libraries like `seaborn`, `matplotlib`, `numpy`, `pandas`, and modules from `sklearn` for machine learning tasks were used.

2. **Loading Data**: Web Scraping Reddit for data, For preparing the public sentiment information dataset we use Reddit, a top social networking platform with comments and posts about Stock market.  SubReddits are categories within the site where all posts regarding a particular topic (category) are compiled, so we'll use the 'StockMarket' subreddit, where all posts related to stock market are posted. I load the dataset from a CSV file named `reddit_posts_labels.csv` using Pandas. The dataset presumably contains Reddit posts and corresponding labels indicating sentiment or some form of classification.

3. **Data Preprocessing**:
I have utilized the praw library to access Reddit's API and scrape data from the "StockMarket" subreddit. This involves setting up a Reddit instance with appropriate authentication credentials (client ID, client secret, user agent) and then fetching posts from the subreddit.
   - Filtering out neutral labels (label 0) from the dataset.
   - Displaying the count of positive (label 1) and negative (label -1) labels.
   
5. **Feature Engineering (Vectorization)**: My script vectorizes the text data (Reddit posts) using CountVectorizer from scikit-learn. This step converts the textual data into numerical features suitable for machine learning algorithms.

6. **Splitting Data**: My script splits the dataset into training and testing sets using train_test_split from scikit-learn.

7. **Handling Class Imbalance**: My script employs Synthetic Minority Over-sampling Technique (SMOTE) from imbalanced-learn to balance the class distribution by oversampling the minority class (label -1).

8. **Model Training and Evaluation**:
   - Training a Multinomial Naive Bayes classifier on the balanced training data.
   - Testing the trained model on the testing data.
   - Calculating accuracy, F1 score, and confusion matrix to evaluate the model's performance.

9. **Comparison with Bernoulli Naive Bayes**: Finally I also attempted training and testing a Bernoulli Naive Bayes classifier but found it less accurate compared to Multinomial Naive Bayes, so it decides to stick with Multinomial Naive Bayes.

Overall, the project performs sentiment analysis on Reddit posts using Naive Bayes classification algorithms and evaluates their performance using accuracy, F1 score, and confusion matrix metrics. It also handles class imbalance using SMOTE to improve the robustness of the model.

