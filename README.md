# Twitter-Bots

Twitter Bots using Node.js interacting with the Twitter API. In the first application, Twitter Favorite Bot - Recent Tweets, the API will allow us to search for tweets, and favorite the tweets that our application finds and the second application, Twitter-Follow-Bot - Popular Tweets, searches for tweets using a query, then follows the user that did the tweeting. 


## Twitter Favorite Bot - Recent Tweets
This bot returns 10 tweets for a specified search query then favorites each of the returned tweets


### How to use

download the repository

run  `npm install`  to install the needed dependencies

Visit the [Twitter API](https://apps.twitter.com/app/new){:target="_blank"} and fill out the form. When done, click on the **Keys and Access Tokens** tab to view your consumer key/secret and access token key/secret. Copy these keys/secrets into your `config.js` file, this file stores the configuration details for the Twitter API. 

The structure should be the following:

```javascript
module.exports = {
  consumer_key: '',
  consumer_secret: '',
  access_token_key: '',
  access_token_secret: ''
}
```

In `app.js` you can edit the params variable to determine what to search for:

```javascript
var params = {
  q: 'SEARCH_QUERY_HERE', //search query
  count: 10, //number of tweets to return
  result_type: 'recent', //shows recent tweets
  lang: 'en' //language English
}
```

### To Run App
Open up the command prompt and type `node app.js` to run the application.  

***  

## Twitter-Follow-Bot - Popular Tweets

This twitter bot follows users based on your inputs. It follows 10 users who recently had popular tweets for a specified search query.


### How to use

In `follow.js` you can edit the params variable to determine what to search for:

```javascript
var params = {
  q: 'SEARCH_QUERY_HERE', //search query
  count: 10, //number of tweets to return
  result_type: 'popular', //shows popular tweets
  lang: 'en' //language English
}
```


### To Run App
Open up the command prompt and type  `node follow.js`  to run the application. 


### References
+ [Build a simple Twitter Bot with Node.js in just 38 lines of code](https://hackernoon.com/build-a-simple-twitter-bot-with-node-js-in-just-38-lines-of-code-ed92db9eb078){:target="_blank"}

+ [Build a simple Twitter Bot with Node.js Part 2: DO MORE](https://hackernoon.com/build-a-simple-twitter-bot-with-node-js-part-2-do-more-2ef1e039715d){:target="_blank"}

+ [Twitter Rest API Reference Documentation](https://dev.twitter.com/rest/reference){:target="_blank"}

