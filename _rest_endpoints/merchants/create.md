---
title: Create a Merchant
description: Creates a new Merchant record.
resource: merchants
type: POST
endpoint: https://api.atpay.com/api/v5/rest/merchants
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/rest/merchants/m_MYGLm6-P_Ap7pgUW-pTrUQ \
   -u key:secret \
   -X POST
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "updated_at" : "2017-02-27T18:43:08.836-07:00",
   "created_at" : "2017-02-27T18:43:08.836-07:00",
   "public_key" : "WRh0g9vIe9F41UWgBR01c6TVCr87Nq7jccqThBua0Ug=",
   "secret_key" : "sk_TIxzaYo82uFHzYmfFIrK3w",
   "private_key" : "5/tFU2MEMTH6yaZvAPJNROOCzFf/zZBBen//4cZZbR4=",
   "authorized_domain" : "https://api.atpay.com",
   "sid" : "m_MYGLm6-P_Ap7pgUW-pTrUQ"
}
{% endhighlight %}
