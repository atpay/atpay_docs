---
title: Create a Button
resource: buttons
description: Creates a new Button record.
type: POST
endpoint: https://authenticate.atpay.com/buttons
arguments:
    - name: amount
      description: Dollar value of button
      data_type: string
      required: true
    - name: payid
      description: Invoice number of other value identifying this payment
      data_type: string
      required: false
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://authenticate.atpay.com/buttons \
  -u key:secret \
  -d amount=9.99 \
  -d payid=1001
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "id"    : "b9b63309-a45f-422c-ac6c-c8f1398b057c",
   "email" : "b9b63309-a45f-422c-ac6c-c8f1398b057c@authenticate.atpay.com"
}
{% endhighlight %}
