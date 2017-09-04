---
category: User
apipath: '/user/{id}/score'
title: "Search user scores"
type: 'GET'

layout: nil
---

Retrieves the list of scores published by a given user. This resource is searchable just like [**`/score`**](#/search-scores)

### Parameters

Name 			 |  Type     | Description     |
:----------------|:----------|:----------------|
**`id`**         | string    | Unique id of the user |

If the user is authenticated, the call will also list the private scores of this user.

### Response

An array of score objects

### Example

{% highlight bash %}
$ curl http://api.musescore.com/services/rest/user/583/score.xml?oauth_consumer_key=your_consumer_key
< HTTP/1.1 200 OK
{% endhighlight %}