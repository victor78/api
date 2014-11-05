---
title: 'Authentication'

layout: nil
---

### Public resources

A number of resources do not require a user to be a authenticated. Only the application needs a valid Consumer Key.  You can request a Consumer Key via email: <api@musescore.com>. Once you have a key, you can pass it as a parameter in a cURL request, or connect to MuseScore.com using just the key.

Examples:  

Using cURL: 
```$ curl 'http://api.musescore.com/services/rest/score?oauth_consumer_key=your_consumer_key```

Note that this won't let you access protected resources.  To do that, you'll need **OAuth**.

### OAuth

To access protected resources you must authenticate with MuseScore.com using OAuth 1.0, a standard to give third party applications the authority to act on a user’s behalf.

If you're not already familiar with OAuth, please read more on [oauth.net](:http://oauth.net/), where there is also a [Getting started](http://oauth.net/documentation/getting-started).

MuseScore.com API is currently private. If you need an OAuth keypair [let us know](http://musescore.com/contact)

### Terminology

**Service Provider**
: MuseScore.com

**Consumer**
: Your Application

**User**
: The user registered with MuseScore.com using your application

### Endpoints

Function | Endpoint |
:-----|:-------------------|
Get a request token        | http://api.musescore.com/oauth/request_token |
User authorization page    | http://musescore.com/oauth/authorize   |
Get an access token        | http://api.musescore.com/oauth/access_token |
