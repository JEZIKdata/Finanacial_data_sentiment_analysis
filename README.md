# Scraping Financial Data To Predict Returns

Have you ever wanted to build an app that tells you **when to buy and sell a stock** based on general public's opinion of it?
We are going to use Twitter to mine public opinion on **NVIDIA** company and build a sentiment-based strategy that helps us predict if we should buy or sell this stock.

For scraping data on Twitter we are going to use **snscrape library** by [JustAnotherArchivist](https://github.com/JustAnotherArchivist/snscrape) that allows one to scrape tweets without the restrictions of Tweepy. Snscrape requires at least Python 3.8 or higher. With snscrape we can pull data into a data frame with filters of our choosing.

**Attributes** available through snscraper Tweet object adn their datatypes: 

***url:*** str, permalink pointing to url location 

***date:*** datetime.datetime, date tweet was created 

***content:*** str, text content of the tweet 

***renderedContent:*** str, text content of the tweet 

***id:*** int, id of tweet 

***user:*** 'User' object containing username, displayname, id, description, descriptionUrls,, verified, created, 
followersCount, friendsCount, statusesCount, favouritedCount, listedCount, mediaCount, location, protected, linkUrl, profileImageUrl, profileBannerUrl 

***outlinks:*** list 

***tcooutlinks:*** list 

***replyCount:*** int, count of replies 

***retweetCount:*** int, count of retweets 

***likeCount:*** int

***quoteCount:*** int, count of users that quoted the tweet and replied 

***conversationId:*** int, same as tweetID 

***lang:*** str, machine generated, assumed language of the tweet 

***source:*** str, where tweet was posted from, Iphone, Android 

***media:*** typing.Optional[typing.List['Medium']] = None, 'Media' object, containing previewUrl, fullUrl, type 

***retweetedTweet:*** typing.Optional['Tweet'] = None, if is retweet, id of original tweet 

***quotedTweet:*** typing.Optional['Tweet'] = None, if is quoted tweet, id of original tweet 

***mentionedUsers:*** typing.Optional[typing.List['User']] = None, 'User' object of any mentioned users in tweet
