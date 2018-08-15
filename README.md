# Fake Review Detection

Online shopping is a fast growing business and shoppers have become more critical, more reliant on product reviews. A survey 
of internet retailer website found that reviews can boost sales by as much as 62%, but a few fake reviews have caused the 
bussiness to be shut down or made a fake product look great.

I built a model using NLP and clustering methods to dectect fake reviews. The current review detection system so far only 
look at the review itself, I believe the information about the user is also very important. It is also included in the model.
The expectation is the model will help us in identifying hidden trend and potential fake reviews, also to find out the users 
that related to these reviews.

The data is the hotel review from data.world.com, it contains 15 megabytes of hotel information, review ratings, text,
username, city, province.

In this model, I use NLTK to preprocess the data, remove stop words, perform stemming, use tf-idf to represent reviews, 
then creat the user information features such as whether the username contains space. Finally, a K-means clustering algorithm 
is applied. From the clustering results,The average ratings in one of the clustering appears extremely high, then I look into 
this cluster and found out that the name under the pattern of firstname associated with a space and one capital letter are giving 
5 star ratings.The main takeaway is the username under the pattern are suspicious users, this information can be used for further
investigation.  

[Find the analysis here](https://github.com/xgao0412/dataIncubatorProject/blob/master/Fake%20review%20inspection%20system.ipynb)
