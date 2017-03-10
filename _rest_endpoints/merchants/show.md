---
title: Retrieve a Merchant
resource: merchants
description: Retrieves specific Merchant object record
type: GET
endpoint: https://api.atpay.com/api/v5/rest/merchants/{{merchant_id}}
arguments:
    - name: merchant_id
      description: Merchant Id
      data_type: string
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/rest/merchants/m_-hnOo_Ef_3KWw6juVeiPGw\
   -u key:secret \
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "sid" : "m_-hnOo_Ef_3KWw6juVeiPGw",
   "private_key" : "iMLOBNvudvDeJqX04lhORPTlFBCyxYP0Ut+yxxRfwiE=",
   "authorized_domain" : "https://api.atpay.com",
   "secret_key" : "sk_k6-oDA2egElF9qc7h5Fcaw",
   "updated_at" : "2016-10-23T20:01:03.348-06:00",
   "public_key" : "by/7MQfBdqkW2mGpUD4mIf2e5cpyYqLDWZFfXafYxTI=",
   "created_at" : "2016-10-23T20:01:03.348-06:00"
}
{% endhighlight %}
