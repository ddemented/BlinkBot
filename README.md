#BLINK Bot - _Chatbot for navigational smart bot_

[![JavaScript Style Guide](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)

##Functionality
####A simple Information and Navigational Chatbot centered around a single institute or society for general Q&A queries.

##Prerequisites
 * Node js
 * NPM
 * express js


 ##To Run with development server :
 #Ngrok:

```node
 npm install
 node index.js
```
Then run the ngrok server on same port (5000) :
```
ngrok http 5000
```

Next configure your webhook on facebook App with server:
-> Enter the ngrok forwarding url + /webhook/ to the callback url, and enter the verify token challenge given in index.js
-> It will verify and save the connection without an error.

Now we run the Curl command from the server to give access for graph api:
```
curl -ik -X POST "https://graph.facebook.com/v2.6/me/subscribed_apps?access_token=<token-id>"
```

-> On Success we have successfully connected the server webhook, and you can say howdy to the bot!
