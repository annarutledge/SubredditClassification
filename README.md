## Problem Statement
Can we build a machine learning model that can distinguish between a 'shower thought' and a 'crazy idea' (based on classification asa post from one of two subredddits, r/Showerthoughts & r/CrazyIdeas)?


## Data Dictionary (for cleaned data)
|Feature|Datatype|Description|
|---|---|---|
|title|string|title of subreddit post|
|text|string or NaN where text is missing|text of subreddit post|
|auth|string|author of subreddit post|
|time|int64|time that post was posted to subreddit (epoch)|
|subreddit|string|subreddit of origin for post (r/Showerthoughts or r/CrazyIdeas)|
|full_text|string|full text of subreddit post - title and text if text is present|
|letter_count|int64|character count of subreddit post|
|word_count|int64|word count of subreddit post|
|subreddit_code|int64|encoded subreddit of origin for post (1 for CrazyIdeas, 0 for Showerthoughts)|


## Executive Summary
#### Is it an insightful shower thought or just a crazy idea?
Chances are, we've all heard someone say that they do their best thinking and have come upon some deep philosphoical musings in the shower. But how true is this? Are so-called shower thoughts really anything special? Or are they just crazy ideas that we come up with when are minds are left to wander?
Being able to distinguish true insightful commentary such as a 'shower thought' from a less impactful or practical 'crazy idea' can help us think more deeply and start conversations that may lead to something meaningful, or at least provide a fun intellectual exercise. 

In order to make this disctinction, we can examine the thoughts of the public, specifically the ones people classify as a shower thought or a crazy idea. The social media platform Reddit provides a great resource for us to do this. By collecting and analyzing examples from two subreddits, r/Showerthoughts and r/CrazyIdeas, we can see what classifies as a shower thought or a crazy idea, and can even build a machine learning model that can automatically help us distinguish between the two. 

We worked towards identifing and building the best-performing model for this task through a process of data collection and cleaning, analysis, and testing of a variety of different classifying models with different modeling paramters that can help them categorize proposed thoughts. These models took in datasets of posts collected from the two relevant subreddits (r/Showerthoughts and r/CrazyIdeas) and using features of this data along with tuning of the aforementioned mdoel parameters, are able to learn how to predict whether the text of a post (or any written out thought submitted to the model) better fits with the 'Shower Thoughts' or the 'Crazy Ideas' category.

After tuning and testing, our best model is able to predict the source of a subreddit post with 83% accuracy! And as time continues we will continue to work on updates and optimization to this modeling system to strive for even more successfull automatic classification.
If you are ready to reflect on your thoughts, and find out if they are deserving of insightful 'shower thought' status, or if you're jsut full of crazy ideas, this is the model for you.


## Results/Conclusions
It is possible to build a machine learning model to distinguish between posts from r/Showerthoughts and r/CrazyIdeas. The best model consturcted in this project was a GradientBoost Classifier which makes predictions with an accuracy of 83%. Going forward this model may be able to be improved with further processing and cleaning of the text-based data utilized and further tuning of model hyperparamaters, particularly with the possibility of tuning an ensemble model that combines the strengths of models tested and achieves even higher accuracy scores.