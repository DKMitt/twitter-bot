# Twitter-Bot

Twitter Bot with Node.js  


## Twitter Favorite Bot - Recent Tweets
This bot returns 10 tweets for a specified search query then favorites each of the returned tweets


### How to use

Star and download the repository

run  npm install  to install the needed dependencies

Edit file named config.js - this file stores the configuration details for the Twitter API. 

The structure should be the following:

```
module.exports = {
  consumer_key: '',
  consumer_secret: '',
  access_token_key: '',
  access_token_secret: ''
}

```

Visit the Twitter API and fill out the form. When done, click on the Keys and Access Tokens tab to view your consumer key/secret and access token key/secret. Copy these keys/secrets into your config.js file.

In app.js you can edit the params variable to determine what to search for:

```

var params = {
  q: 'SEARCH_QUERY_HERE', //search query
  count: 10, //number of tweets to return
  result_type: 'recent', //shows recent tweets
  lang: 'en' //language English
}

```

### To Run App
Open up the command prompt and type node app.js to run the application.

  

## Twitter-Follow-Bot - Popular Tweets

This twitter bot follows users based on your inputs. It follows 10 users who recently had popular tweets for a specified search query.


### How to use

In follow.js you can edit the params variable to determine what to search for:

var params = {
  q: 'SEARCH_QUERY_HERE', //search query
  count: 10, //number of tweets to return
  result_type: 'popular', //shows popular tweets
  lang: 'en' //language English
}


### To Run App
Open up the command prompt and type  node follow.js  to run the application. 
