---
title: Create a Gateway
resource: gateway
description: Creates a new Gateway record.
type: POST
endpoint: https://api.atpay.com/api/v5/rest/gateways
arguments:
    - name: type
      description: description
      required: true
    - name: credentials
      description: a hash of the gateway's required credentials
    - name: default
      description: set as default gateway
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/rest/gateways \
   -u key:secret \
   -d type=test \
   -d default=true
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "created_at" : "2017-02-27T13:10:37.910-07:00",
   "status" : "Active",
   "name" : "Spreedly Test",
   "id" : "gw_PkCqHWQdT7iVgp83BOo-Ww",
   "default" : true
}
{% endhighlight %}
