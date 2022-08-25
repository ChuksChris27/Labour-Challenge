# #LabourChallenge Twitter Scraping Documentation

Sometime in 2022, the APC Presidential Candidate made a statement that the people would labour in vain. 
This sparked various reactions on twitter and birthed new hashtags - ```The Labour Challenge and Dignity in Labour``` hashtags. 

Various tweets containing keywords such as 'Our labour will not be in vain' were made with the hashtag.

## The Task

I decided to scrape Twitter's API using the hashtag as keyword. I scraped a month's worth of data for it's following content:
- Tweet ID
- Username
- Tweet
- Like Count
- Retweet Count
- Source of Tweet
- Coordinates
- Location
- Date Created

After that I performed some data cleaning processes

### Libraries Used

I also imported various libraries such as
- Pandas
- Numpy
- Snscrape
- re #In-built regular expressions library
- string
- nltk
- TextBlob # TextBlob - Python library for processing textual data

#### Natural Language Processing Toolkit
- Stopwords, Words #get stopwords from NLTK library & get all words in english language
- Word_tokenize #to create word tokens
- Pos_tag #For Parts of Speech tagging

### The Data Extraction Process

For this process, I opted to use 'SNSCRAPE'. This is because it allows me to get twitter data older than 7 days, unlimited amount of tweets, and has no need for API keys

I extracted my data in two folds
- I used Snscrape to get my location data in either to get coordinates (longitude and latitude)
- I used Snscrape to get actual data for my preferred choice of columns

I searched Twitter for two different Keywords
- #labourchallenge
- #dignityinlabour

After which, I merged my datasets and cleaned further.

### The Data Cleaning Process

The following processes to clean my data was done:
- I dropped unnecessary columns
- I merged datas
- I renamed columns
- I removed URL links from the Tweet columns
- Converted strings to their proper cases
- I obtained necessary columns using Natural Language Processing Toolkit
- Replace Strings using 'str.contains'
- Filled null values in the coordinate columns and replaced strings appropriately
- Classified locations
- Filled null values in Location columns
- Separated the Date Created columns into different columns of Day, Month, Year, Hour
- Performed Sentimental Analysis

### Total Shape of Final Data

The entire data collated had 19,977 columns and 23 rows

The entire code process is found in the Labour Challenge.ipynb file in this repository.
I am open for corrections, code adjustments and contributions

## Data Visualization
The final data was downloaded and Visualized using Power BI.
The Power BI file is found in this repository

Reference Link - ```https://github.com/jess-data/Twitter-2020-Sentiment-Analysis/blob/master/Twitter%20Sentiment%20Analysis%20Project.ipynb```
