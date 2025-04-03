
# Web Scraping and Sentiment Analysis on British Airways Reviews from [SKYTRAX](https://www.airlinequality.com/airline-reviews/british-airways)

## Overview

This project involves web scraping data from the [SKYTRAX](https://www.airlinequality.com/airline-reviews/british-airways) website, performing text preprocessing, topic modeling, and sentiment analysis. The goal is to extract valuable insights from the user reviews, such as sentiment trends and common topics, and to visualize the data.

## Resources Used

The following libraries and tools were utilized for this project:

- **Web Scraping**: `requests`, `BeautifulSoup`
- **Data Handling**: `csv`, `pandas`
- **Natural Language Processing (NLP)**: 
  - `spacy` (for lemmatization and tokenization)
  - `nltk` (for stop word removal, stemming)
- **Text Analysis**: 
  - `LatentDirichletAllocation` (for topic modeling)
  - `CountVectorizer` (for text feature extraction)
- **Sentiment Analysis**: `VaderSentiment` (for sentiment analysis)
- **Visualization**: 
  - `WordCloud` (for visualizing frequent terms)
  - `matplotlib` (for creating plots)

## Steps and Process

### 1. **Web Scraping**

We begin by scraping data from the SKYTRAX website, which typically includes user reviews for airlines and airports. The following steps are performed:

- Sending requests to the website.
- Parsing the HTML content using `BeautifulSoup`.
- Extracting relevant data (e.g., reviews, ratings, etc.).
- Storing the scraped data into a CSV file for further processing.

### 2. **Text Preprocessing**

Once the data is scraped, we perform several preprocessing steps to clean and prepare the text data for analysis:

- **Tokenization**: Splitting text into individual words or tokens.
- **Stop Word Removal**: Removing common words (e.g., 'the', 'and', 'is') that don’t contribute much to the meaning.
- **Lemmatization**: Reducing words to their base or root form (e.g., "running" becomes "run").
- **Stemming**: Further simplifying words to their root forms (e.g., "flying" becomes "fli").
- **Cleaning**: Removing unwanted characters, URLs, and other noise from the text.

### 3. **Topic Modeling**

Using **Latent Dirichlet Allocation (LDA)**, we identify the underlying topics within the reviews. This helps in understanding common themes discussed by users. We use **CountVectorizer** to convert the text into a bag-of-words model before applying LDA.

### 4. **Sentiment Analysis**

The sentiment of each review is analyzed using **VaderSentiment**. Sentiment scores are calculated based on the text's tone, ranging from positive, negative, or neutral sentiment. These scores are useful for understanding customer sentiment over time or for particular airlines.

### 5. **Visualization**

We create visualizations to present the insights gained:

- **Word Cloud**: A visual representation of the most frequent words in the reviews.
- **Sentiment Distribution**: A plot showing the distribution of sentiments across the dataset.

## Installation and Setup

To run this project, you will need to install the following dependencies:

```bash
pip install requests beautifulsoup4 pandas spacy nltk vaderSentiment wordcloud matplotlib scikit-learn
```

Additionally, you'll need to download the necessary `nltk` datasets:

```python
import nltk
nltk.download('stopwords')
```

For **spaCy**, you'll also need to download the language model:

```bash
python -m spacy download en_core_web_sm
```

## How to Use

1. Clone this repository to your local machine.
2. Run the script that scrapes data from the SKYTRAX website.
3. After scraping, follow the steps in the script to preprocess the text data and perform topic modeling and sentiment analysis.
4. View the results, including sentiment analysis scores and topic visualizations, in the output files and plots.

## Example Output

- Sentiment scores (positive, negative, neutral) for each review.
- A topic model showing the most common themes discussed in the reviews.
- Word clouds displaying frequently mentioned terms.
  
## Conclusion

This project provides valuable insights into customer sentiments and frequently discussed topics in user reviews from SKYTRAX. It combines web scraping, text preprocessing, topic modeling, and sentiment analysis to create a comprehensive analysis of customer feedback.

---
