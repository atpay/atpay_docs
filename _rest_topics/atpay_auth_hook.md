---
title: Atpay Auth -  Response Hook
description: Hook sent in response to a authentication request.
response_fields:
    - name: button_id
      description: ID of the button being authenticated
      data_type: string
    - name: payer_email
      description: Email address being authenticated
      data_type: string
    - name: auth_result
      description: Boolean indicating whether or not the email could be authenticated
      data_type: boolean
    - name: amount
      description: Amount of the button
      data_type: string
    - name: pay_id
      description: Invoice number of other value identifying this payment
      data_type: string
layout: hook_doc
---

## Example Hook
{% highlight json %}
{
   "button_id"    : "b9b63309-a45f-422c-ac6c-c8f1398b057c",
   "payer_email"  : "patrickw@atpay.com",
   "auth_status"  : true,
   "amount"       : "9.99",
   "pay_id"       : "1001"
}
{% endhighlight %}
