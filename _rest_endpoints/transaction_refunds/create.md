---
title: Create Transaction Refund
resource: transaction-refunds
description: Refunds a previously processed Transaction.
type: GET
endpoint: https://api.atpay.com/api/v5/rest/transactions/refunds
arguments:
    - name: transaction
      description: Unique identifier for Transaction.
      data_type: string
      required: true
    - name: user
      description: Identifier for user processing transaction.
      data_type: string
    - name: notes
      description: Notes for reason of transaction.
      data_type: string
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/rest/transactions/refunds \
  -u key:secret \
  -d transaction='63BF8A72-DEA5-4A24-83A4-F7F29835BC70' \
  -d user='admin@example.com' \
  -d notes='Reason for refund.' | json_pp
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "transaction" : {
      "amount" : "100.0",
      "merchant" : "m_-hnOo_Ef_3KWw6juVeiPGw",
      "net_amount" : null,
      "offer" : {
         "id" : "3D25EE85-0908-4EA6-A5A8-544A62ED9A45",
         "details" : null,
         "tag" : null,
         "item_name" : "Payment of $100.00.",
         "signup_url" : "https://localhost:5000/offers/3D25EE85-0908-4EA6-A5A8-544A62ED9A45?",
         "form" : null,
         "campaign" : null,
         "ref_id" : null
      },
      "user_data" : {
         "offer_confined_gateway" : "gw_c48uefrgwkY3GrlEk7vO7g",
         "demo" : "1",
         "amount" : "100",
         "custom_data" : {},
         "shipping" : null,
         "billing" : {
            "street2" : "",
            "state" : "NM",
            "phone" : "",
            "city" : "Albuquerque",
            "zip" : "87105",
            "street" : "123 Street Rd. NW"
         }
      },
      "source" : "Web Transaction",
      "gateway" : "gw_c48uefrgwkY3GrlEk7vO7g",
      "refund" : {
         "refunded_reason" : "Reason for refund.",
         "refunded_token" : "8GMMzpjfxCNJcy66eOMPp7WIpgA",
         "refunded_by" : "admin@example.com",
         "refunded_at" : "2017-03-02"
      },
      "id" : "63BF8A72-DEA5-4A24-83A4-F7F29835BC70",
      "created_at" : "2017-03-01T16:51:41.457-07:00",
      "customer" : {
         "atpay_token" : "NzAxMGU5ZjkyOVg/kmaMpQA=",
         "sms_number" : null,
         "card_type" : "visa",
         "card_mask" : "1111",
         "email" : "demo@example.com",
         "expiration_date" : "2022-01-01",
         "billing_address" : "123 Street Rd. NW, Albuquerque NM, 87105",
         "last_name" : "Doe",
         "first_name" : "John"
      },
      "status" : "Refunded"
   }
}

{% endhighlight %}
