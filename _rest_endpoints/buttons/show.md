---
title: Retrieve an Button
resource: buttons
description: Retrieves specific Button object record
type: GET
endpoint: https://authenticate.atpay.com/buttons/{{id}}
arguments:
    - name: id
      description: The unique identifier of the Button object
      data_type: string
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://authenticate.atpay.com/buttons/b9b63309-a45f-422c-ac6c-c8f1398b057c \
  -u key:secret
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "id"     : "b9b63309-a45f-422c-ac6c-c8f1398b057c",
   "amount" : "9.99",
   "payid"  : "1001",
   "email"  : "b9b63309-a45f-422c-ac6c-c8f1398b057c@authenticate.atpay.com"
}
{% endhighlight %}
