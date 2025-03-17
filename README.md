# Social-Media-Data-Analysis-on-Sustainability
 
ABSTRACT:
Social media data plays a significant role in understanding the society’s perspective of a particular situation. Social media platforms such as twitter enables users to post their unfiltered opinions in the form of tweets. These tweets can be used as a powerful tool to understand people’s point of view in the domain of our interests such as environmental sustainability. Our project focuses on analysing twitter users tweets based on topics related to environmental sustainability and analyse the public sentiments. In this we’ve performed sentimental analysis on the tweets using BERT model and based on those sentiment labels we have performed various analysis measures to uncover new levels of detail about human-environment interactions. This report focuses on the opportunities , threats and challenges associated with the use of social media data in sustainability.


INTRODUCTION:
The integration of social media data into environmental sustainability research presents significant opportunities and challenges. Social media platforms such as Twitter, Facebook, and Instagram represent volumes of data that are increasingly integral to research into environmental sustainability. By analysing this data, researchers uncover new levels of detail about human-environment interactions, track changes, and engage the public in sustainability issues. This report summarizes the key themes identified from this critical review which emphasis on both opportunities and challenges associated with the use of social media data in sustainability.
OPPORTUNITIES:
Social media data offer a unique insight into public opinion and behaviour about the environment. Using such data, researchers can track how people discuss climate change, renewable energy, and other sustainability issues. This information can help assessing the impact of environmental policies, and understand how people respond to natural disasters.
1.Understanding Human-Nature Interactions:  The knowledge from this data is crucial in showing behavioural patterns, public perception about environmental policies, and responses towards natural hazards.

2. Real-Time Monitoring: The real-time nature of social media communication enables continuous monitoring of environmental changes and social responses. This is particularly useful in disaster risk reduction, where timely data can inform rapid responses to events like floods, wildfires, and hurricanes.
3. Public Engagement and Awareness: Social media is one of the most influential tools for increasing awareness and engaging the public on environmental issues. By analysing social media content, researchers can measure public sentiment, track the spread of sustainability messages, and understand the dynamics involved.

THREATS AND ETHICS:
However, there are many issues with using social media data. Most often, the data available to researchers is restricted by the social media companies themselves, making it difficult to gather deep longitudinal data. Then, there are ethical issues concerning user privacy and ensuring that data is used in a manner that is responsible. In addition, social media data may be biased since it may not depict all demographic groups in equal measure. 
1.Data Accessibility: Social media platforms control access to their data, and they can change their rules, limit access, or even shut down. This makes it hard for researchers who need stable, long-term data access. 
2.Ethical Concerns: Using social media data comes with ethical challenges. Researchers need to be careful about privacy, getting user consent, and keeping data secure. The Cambridge Analytica scandal showed how important it is to follow strict ethical guidelines.
 3.Data Biases: Social media data can be biased because it reflects the demographics of users, how platforms prioritize content, and what users choose to share. These biases can affect research results, making them less representative of different regions or groups of people.

DATASET COLLECTION:
We’ve collected the tweets based on sustainability by a web scrapping tool called Bardeen.ai by specifying the keywords such as disasters, sustainability development, climatic changes that we would want to extract from the tweets.
The features of our dataset include:
 Name: The name of the Twitter user.
Handle: The Twitter username or handle of the user.
Media URL: Link to any media (images, videos) included in the tweet.
Retweets: Count of retweets received by the tweet.
Likes: Count of likes received by the tweet.
Comments: Count of comments or replies to the tweet.
Views: Count of views the tweet has received.
Tweet URL: Link to the original tweet.
Profile Link: Link to the user’s profile.
Post Body: The full, original text content of the tweet.
Date: Date when the tweet was posted.
Timestamp: Exact time when the tweet was posted.
TWEET PRE-PROCESSING:
Since the tweets may be in different formats such as the case, special characters and non-english characters we need to bring the tweets to a standaradized format. In-order to do sentimental analysis, the model understands the tweets only if it is the standard format we’ve used text pre-processing library known as NLTK which was used for performing tokenization and lemmatisation, it includes a new feature cleaned post body.
Cleaned Post Body: Processed and cleaned version of the tweet’s text, for sentiment analysis.
SENTIMENTAL ANALYSIS:
The sentiments of the tweets were analysed to categorize it into two labels: positive and negative. We tested three models and chose the model which gave the highest accuracy.
bert-base-uncased accuracy: 0.9444
roberta-base accuracy: 0.9444
distilbert-base-uncased-finetuned-sst-2-english accuracy: 0.6889

Best model: bert-base-uncased with accuracy 0.9444
Since the BERT model gave the highest accuracy it was chosen to label the tweets based on their sentiments, which provided the inclusion of a new feature sentiments.
Sentiment: Sentiment label (e.g., positive or negative) assigned to the tweet content for analysis.
DATA PRE-PROCESSING:
The data should be cleansed before processing. For that we formatted the data based on the date and handled missing value if it existed for categorical features we’ve replaced by using mode and for continuous features we’ve replaced by using it’s mean.
DATA SIMULATION:
Since the above features cannot be represented as a graph with nodes and edges as there is no relationship to be considered for drawing an edge. We’ve simulated three more features based on the values of the existing features.
followers_count: The number of followers the Twitter user has, indicating their reach and influence. It is based on retweets count.
retweeted_by: A list or count of specific users who retweeted the tweet, showing engagement from particular accounts.
mutual_friends: Users who are followed by both the tweet’s author and other specified users, helping to identify shared connections in the network.



VISUALIZATIONS WITH INFERENCE:

 Distribution of Followers Count
