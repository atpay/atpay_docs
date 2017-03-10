---
title: Retrieve Recurring Payments
resource: recurring-payments
description: Lists all Recurring Payment objects associated with Merchant.
type: GET
endpoint: https://api.atpay.com/api/v5/rest/recurring_payments
layout: api_doc
---

## Example Request
{% highlight bash %}
  curl https://api.atpay.com/api/v5/rest/recurring_payments -u key:secret
{% endhighlight %}

## Example Response
{% highlight json %}
[
   {
      "next_payment_date" : "2017-02-23",
      "transaction" : {
         "amount" : "100.0",
         "credit_card" : {
            "email" : "demo@example.com"
         }
      },
      "created_at" : "2017-01-05T10:43:04.149-07:00",
      "id" : 1,
      "offer_id" : 354,
      "updated_at" : "2017-02-16T00:24:09.696-07:00",
      "frequency" : "weekly"
   },
   {
      "updated_at" : "2017-02-16T00:24:09.697-07:00",
      "frequency" : "weekly",
      "next_payment_date" : "2017-02-23",
      "transaction" : {
         "amount" : "100.0",
         "credit_card" : {
            "email" : "demo@example.com"
         }
      },
      "id" : 2,
      "created_at" : "2017-02-02T10:56:37.985-07:00",
      "offer_id" : 421
   }
]
{% endhighlight %}
