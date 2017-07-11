---
title: Authentication
layout: api_doc
---
To authenticate API calls, the @Pay API uses HTTP Basic Auth. Use your Organization's API Key as your username and your Organization's and API Secret as your password. All API requests must be made over HTTPS.


If you would like to request access to the API or feel as if your credentials have been compromised, please email info@atpay.com.


## Example Request
{% highlight bash %}
  $ curl https://app.atpay.com/api/v5/rest/transactions -u key:secret
{% endhighlight %}
