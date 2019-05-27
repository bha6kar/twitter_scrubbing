# Twitter Scrubbing

### Twitter Scrapping
The data with which I am going to work is a list of tweets with the hashtag #AAPL from 16 May 2019 to 27 May 2019. Dataset is composed by 43 columns. But only a few columns will be concerned for the analysis. In this analysis I kept the column “text” which contains the text of the tweet, the column “created at” which contains the tweet time posted.

### Data Cleaning
```
b'RT @ArgentArts: Albrecht #Durer #iPhone #Case\n\nhttps://t.co/WpQa11PA8O\n\n#iphonecase $AAPL https://t.co/if4tzbDv5o'
```
You can see that in the first tweet we can find an URL, punctuation's and a username of one tweets (preceded by @). Before the data visualisation or the sentiment analysis it is necessary to clean the data. 
Also there are many retweets, like RT at start above shows retweet. To avoid getting retweets I filtered the data first only take the original tweets and filter out the retweets.

```
b'Apple (AAPL) Holder Stonehearth Capital Management Increased Holding; Parus Finance Uk LTD Lowered Its Apple (AAPL)\xe2\x80\xa6 https://t.co/fCh5CXSlRI'
```
Now retweets are filtered, but still the tweet consists of many useless data. so for that I
Delete the certain punctuation's, the URLs, put the text in lower case and delete the double space, and put the text in a lower case, extract the tweet for examples. It is possible to add more steps but in my case it won’t be useful, as I am only considering tweets and posted time.
After cleaning the text it looks like below text, which is more clear and human readable:

```
Bitcoin 8085 vs AAPL 1802 25 1 week 36 1032 YTD 137
```

### Twitter Sentiment

After cleaning the data. I am going to do sentiment analysis. Semtimental analysis can be done by many sentimental libraries like VADER, TEXTBLOB, but for this time I am going to use TextBlob. The objective is to class by type the tweets. So for that I'm going to distinguish 3 kinds of tweets according to their polarity score calculated by TextBlob for the tweet. We will have the positive tweets, the neutral tweets, and the negative tweets.
If the tweet polarity is more than 0 it will be 'POSITIVE' or if less than 0 it will be 'NEGATIVE' else it will be 'NEUTRAL'.

### Data Visualisation

I plot the data of sentiment on bar graph to see how many tweets are positive, negative or neutral, as the data will lie between -1 to 1.

![Figure](/Figure_1.png)


