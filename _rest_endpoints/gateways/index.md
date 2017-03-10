---
title: List all Gateways
resource: gateway
description: Lists all Gateway objects associated with Merchant.
type: GET
endpoint: https://api.atpay.com/api/v5/rest/gateways
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/rest/gateways \
   -u key:secret
{% endhighlight %}

## Example Response
{% highlight json %}
[
    {
        "created_at": "2016-10-27T13:45:40.809-06:00",
        "default": false,
        "id": "gw_9rZsMjyfOhJbCdhTKiO3Ow",
        "name": "Stripe",
        "status": "Active"
    },
    {
        "created_at": "2016-10-27T21:34:14.603-06:00",
        "default": false,
        "id": "gw_4lWffYmgNcPAi4lKt9TO_A",
        "name": "Stripe",
        "status": "Active"
    }
]
{% endhighlight %}
