# Reddit_score_predictor

This is a repository for my project on predicting if a submission to Reddit will be high-scoring.
The code is provided as a Jupyter notebook and there is a csv file containing the data.

For this project, I analyse the submission specifically to the r/britishproblems subreddit. The reason for choosing this subreddit is almost all submissions are purely text based, i.e., don't contain images and links, which would make it much harder to classify the features that make a submission high-scoring. 
Also, because the expected users of this subreddit will primarly be people from the U.K., it makes it easier when analysing and drawing conclusions from the data, e.g., having a low number of submissions between 12pm and 6am is expected as it would be nighttime in the U.K. 
Finally, it's also interesting looking at the data which gives an insight into what people here in the U.K. are likely to upvote, and when they use Reddit.

The data for this model is made by using the Reddit API to collect new submissions from the subreddit 'hot' section. It is then used to train a neural network, using natural language processing of the submission titles, with tokenising and embedding, and also categorical features such as the day of the week. Because of the mixed data types, the model is comprised of two networks - one for the text and one for the categorical features - which are then joined to a single binary output.
