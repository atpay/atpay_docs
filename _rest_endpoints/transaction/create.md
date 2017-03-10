---
title: Create a Transaction
resource: transactions
description: Processes and creates a new Transaction record.
type: GET
endpoint: https://api.atpay.com/api/v5/rest/transactions
arguments:
    - name: atpay_offer
      description: Unique identifier of @Pay Offer object.
      data_type: string
      required: true
    - name: token
      description: Unique identifier of @Pay Credit Card object.
      data_type: string
      required: true
layout: api_doc
---


processor = ApiRequest::TransactionProcessor.new(params[:atpay_offer], params[:token], @merchant)


## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/rest/transactions \
  -u key:secret \
  -d atpay_offer=1 \
  -d token=100
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "transaction" : {
      "created_at" : "2017-03-01T16:51:41.457-07:00",
      "status" : "Successful",
      "offer" : {
         "ref_id" : null,
         "details" : null,
         "item_name" : "Payment of $100.00.",
         "signup_url" : "https://localhost:5000/offers/3D25EE85-0908-4EA6-A5A8-544A62ED9A45?",
         "campaign" : null,
         "id" : "3D25EE85-0908-4EA6-A5A8-544A62ED9A45",
         "tag" : null,
         "form" : null
      },
      "net_amount" : null,
      "amount" : "100.0",
      "merchant" : "m_-hnOo_Ef_3KWw6juVeiPGw",
      "gateway" : "gw_c48uefrgwkY3GrlEk7vO7g",
      "customer" : {
         "sms_number" : null,
         "expiration_date" : "2022-01-01",
         "email" : "demo@example.com",
         "billing_address" : "123 Street Rd. NW, Albuquerque NM, 87105",
         "last_name" : "Doe",
         "card_mask" : "1111",
         "atpay_token" : "NzAxMGU5ZjkyOVg/kmaMpQA=",
         "first_name" : "John",
         "card_type" : "visa"
      },
      "user_data" : {
         "billing" : {
            "state" : "NM",
            "city" : "Albuquerque",
            "street" : "123 Street Rd. NW",
            "street2" : "",
            "zip" : "87105",
            "phone" : ""
         },
         "demo" : "1",
         "offer_confined_gateway" : "gw_c48uefrgwkY3GrlEk7vO7g",
         "custom_data" : {},
         "amount" : "100",
         "shipping" : null
      },
      "source" : "Web Transaction",
      "id" : "63BF8A72-DEA5-4A24-83A4-F7F29835BC70"
   },
   "errors" : null
}
{% endhighlight %}
