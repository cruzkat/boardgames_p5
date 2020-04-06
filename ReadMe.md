# Project 5: Predicting Board Game Success (Popularity)

For my final Metis project, I looked into what makes a board game popular. As a board game enthusiast, it has been wild to see the hobby explode in recent years. With more games on the market than ever before, I wanted to see if there were any common themes or features that determine a game's popularity. This can be useful for board game creators as well as enthusiasts/investors looking for what games to fund on Kickstarter or similar platforms.

I used 2 Kaggle datasets from BoardGameGeek for this analysis. The first contains 13 million reviews and game attributes for board games and the second contains more in-depth board game attributes. There are 4 notebooks for this data.

### 1. Gathering the Data (bgg_data)
The first notebook with combines the game attributes from both datasets into one dataframe. I also filter through all review data and combine all text reviews for a game into one long text string. Both of these dataframes are pickled for use in subsequent notebooks.

### 2. Exploratory Data Analysis (bgg_game_eda)
By visualizing the distributions of various features, I learned what needed to be scaled. I also created a few new features like average players and average game time that combined separate features (min / max time & players). 

### 3. Text Processing (bgg_textpreprocessing)
Cleaning the text reviews by removing punctuation and stopwords. Using NLTK, I lemmatized the text and also extracted nouns and adjectives. Once cleaned, I compared Count Vectorizer and TF-IDF with various models (LSA, LDA, NMF). I end the notebook with my finalized topics.   

### 4. Regression Modeling (bgg_modeling)
With the game features and game reviews combined into one dataframe, this notebook shows various different regression models.