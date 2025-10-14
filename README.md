 Task 3: NLP Sentiment Analysis
 -Project Goal
This project implements a Natural Language Processing (NLP) pipeline to perform Sentiment Analysis on a provided dataset of textual data. The objective is to automatically classify the sentiment of each text entry as Positive, Negative, or Neutral, and to visualize the findings to gain insights into overall public or customer opinion.

Technical Stack & Libraries
Component	Tool/Library	Purpose
Language	Python	Core scripting and analysis environment.
Data Handling	Pandas	Loading, cleaning, and structuring the dataset.
NLP/Text Cleaning	NLTK	Tokenization, removing stop words, and Lemmatization.
Sentiment Analysis	TextBlob	Calculating the Polarity Score for sentiment classification.
Visualization	Matplotlib, Seaborn, WordCloud	Generating charts for sentiment distribution and word frequency.


- Dataset
The analysis uses the proprietary dataset provided for the task:
File Name: 3) Sentiment dataset.csv
Key Column: Text (This column contains the raw data for sentiment extraction).

-Methodology
1. Data Loading and Initial Setup
The Sentiment dataset.csv file was loaded into a Pandas DataFrame.
Necessary NLP libraries (nltk, TextBlob) and their required resources were installed and downloaded.

2. Text Preprocessing (Cleaning)
This crucial step prepares the raw text for accurate analysis:
Cleaning: Removed special characters, punctuation, and converted all text to lowercase.
Tokenization: Broke down sentences into individual words (tokens).
Stop Word Removal: Eliminated common, non-informative words (e.g., 'the', 'is', 'a').
Lemmatization: Reduced words to their base or root form (e.g., 'running' → 'run') to minimize feature space.

3. Sentiment Calculation and Classification
Polarity Scoring: The TextBlob library was applied to the cleaned text to calculate a polarity_score (ranging from -1.0 (most negative) to +1.0 (most positive)).
Classification: A custom function classified the scores into three discrete categories using defined thresholds:
Positive (Score > 0.05)
Negative (Score < -0.05)
Neutral (Score between -0.05 and 0.05)

4. Visualization and Insight Generation
Two key visualizations were generated to summarize the findings:
Sentiment Distribution Bar Chart: Shows the total count and proportion of Positive, Negative, and Neutral entries.
Word Clouds: Generated a Word Cloud for the entire corpus to identify general themes, and optionally, a separate one for Negative text to pinpoint specific pain points or complaints.
