---
title: List all Transactions
resource: transaction
description: Lists all Transaction objects associated with Merchant.
type: GET
endpoint: https://api.atpay.com/api/v5/rest/transactions
layout: api_doc
---

## Example Request
{% highlight bash %}
  curl https://api.atpay.com/api/v5/rest/transactions -u key:secret
{% endhighlight %}

## Example Response
{% highlight json %}
[
   {
      "amount" : "100.0",
      "offer" : {
         "item_name" : "Payment of $100.00.",
         "form" : "f_YxMtY3gTW1BlqHaUgIvrSg",
         "campaign" : "your-campaign-14",
         "signup_url" : "http://localhost:4000/offers/?",
         "id" : "B718DD97-BD7E-4888-AB67-557CC13B16B9",
         "ref_id" : null,
         "tag" : null,
         "details" : ""
      },
      "id" : "CF692438-A9D1-4195-942E-D22D8988E09E",
      "net_amount" : null,
      "gateway" : "gw_c48uefrgwkY3GrlEk7vO7g",
      "user_data" : {
         "form" : "f_YxMtY3gTW1BlqHaUgIvrSg",
         "billing" : {
            "city" : "Albuquerque",
            "phone" : "",
            "street2" : "",
            "state" : "NM",
            "street" : "123 Street Rd. NW",
            "zip" : "87105"
         },
         "recurring_frequency" : "once",
         "custom_data" : {},
         "offer_confined_gateway" : "gw_c48uefrgwkY3GrlEk7vO7g",
         "campaign" : "your-campaign-14",
         "offer_token" : "",
         "amount" : "100.00",
         "tags" : "",
         "signup_url" : "http://localhost:4000/offers/",
         "merchant_id" : "m_-hnOo_Ef_3KWw6juVeiPGw",
         "shipping" : null,
         "item_details" : ""
      },
      "source" : "Web Transaction",
      "merchant" : "m_-hnOo_Ef_3KWw6juVeiPGw",
      "created_at" : "2017-02-23T13:04:48.428-07:00",
      "status" : "Successful",
      "customer" : {
         "email" : "demo@example.com",
         "last_name" : "Doe",
         "expiration_date" : "2022-01-01",
         "card_type" : "visa",
         "sms_number" : "5555555555",
         "atpay_token" : "OGM1NGRmODk5YlivQF+MpQA=",
         "billing_address" : "123 Street Rd. NW, Albuquerque NM, 87105",
         "first_name" : "John",
         "card_mask" : "1111"
      }
   },
   {
      "user_data" : {},
      "created_at" : "2017-02-23T13:04:31.778-07:00",
      "merchant" : "m_-hnOo_Ef_3KWw6juVeiPGw",
      "source" : "Web Transaction",
      "status" : "Failed",
      "customer" : {
         "billing_address" : "123 Street Rd. NW, Albuquerque NM, 87105",
         "card_mask" : "1112",
         "first_name" : "John",
         "expiration_date" : "2022-01-01",
         "email" : "demo@example.com",
         "last_name" : "Doe",
         "card_type" : "visa",
         "atpay_token" : "MjdjNmI3NmQyM1ivQE+MpQA=",
         "sms_number" : "5555555555"
      },
      "errors" : {
         "general" : "Invalid Card"
      },
      "id" : "569DD192-EC91-4F19-8329-C12E36D03A43",
      "offer" : {
         "campaign" : "your-campaign-14",
         "form" : "f_YxMtY3gTW1BlqHaUgIvrSg",
         "item_name" : "Payment of $100.00.",
         "details" : "",
         "tag" : null,
         "ref_id" : null,
         "id" : "B718DD97-BD7E-4888-AB67-557CC13B16B9",
         "signup_url" : "http://localhost:4000/offers/?"
      },
      "amount" : "100.0",
      "net_amount" : null,
      "error" : "Invalid Card",
      "gateway" : "gw_c48uefrgwkY3GrlEk7vO7g"
   },
   {
      "offer" : {
         "id" : "B718DD97-BD7E-4888-AB67-557CC13B16B9",
         "signup_url" : "http://localhost:4000/offers/?",
         "details" : "",
         "tag" : null,
         "ref_id" : null,
         "form" : "f_YxMtY3gTW1BlqHaUgIvrSg",
         "item_name" : "Payment of $100.00.",
         "campaign" : "your-campaign-14"
      },
      "id" : "5CDADCCF-8FDC-457F-A2D1-DC2B6FD5F6ED",
      "amount" : "100.0",
      "errors" : {
         "general" : "Invalid Card"
      },
      "gateway" : "gw_c48uefrgwkY3GrlEk7vO7g",
      "error" : "Invalid Card",
      "net_amount" : null,
      "status" : "Failed",
      "merchant" : "m_-hnOo_Ef_3KWw6juVeiPGw",
      "source" : "Unavailable",
      "created_at" : "2017-02-23T13:02:48.573-07:00",
      "user_data" : {},
      "customer" : {
         "card_mask" : "1112",
         "first_name" : "John",
         "billing_address" : "123 Street Rd. NW, Albuquerque NM, 87105",
         "sms_number" : "5555555555",
         "atpay_token" : "NGI1MGFmZDNmZlivP+aMpQA=",
         "card_type" : "visa",
         "last_name" : "Doe",
         "email" : "demo@example.com",
         "expiration_date" : "2022-01-01"
      }
   }
]
{% endhighlight %}
