---
title: List all Credit Cards
resource: credit-cards
description: Lists all Credit Card objects associated with Merchant.
type: GET
endpoint: https://api.atpay.com/api/v5/rest/credit_cards
layout: api_doc
---

## Example Request
{% highlight bash %}
 curl https://api.atpay.com/api/v5/rest/credit_cards -u key:secret
{% endhighlight %}

## Example Response
{% highlight json %}
[
   {
      "phone" : "",
      "successful" : true,
      "street" : "123 Street Rd. NW",
      "state" : "NM",
      "email" : "demo@example.com",
      "auth_token" : "Dnp7vkZF7ypCBLF05eJDYVqaLaP",
      "street2" : "",
      "id" : 97,
      "card_type" : "visa",
      "last_name" : "Doe",
      "zip" : "87105",
      "transaction_errors" : null,
      "one_time_use" : false,
      "reusable" : true,
      "updated_at" : "2016-11-30T20:00:55.953-07:00",
      "first_name" : "John",
      "data" : {
         "amount" : null,
         "guest" : "0",
         "sms_number" : null,
         "buyer_data" : "{\"billing\":{\"street\":\"123 Street Rd. NW\",\"street2\":\"\",\"city\":\"Albuquerque\",\"state\":\"NM\",\"zip\":\"87105\",\"phone\":\"\"},\"shipping\":null}",
         "email_opt_in" : "0"
      },
      "third_party_token" : null,
      "atpay_token" : "NzAxMGU5ZjkyOVg/kmaMpQA=",
      "redacted_at" : null,
      "email_opt_in" : false,
      "country" : "",
      "created_at" : "2016-11-30T20:00:54.069-07:00",
      "expiration_date" : "2022-01-01",
      "city" : "Albuquerque",
      "sms_number" : null,
      "card_mask" : "1111"
   },
   {
      "one_time_use" : false,
      "first_name" : "John",
      "updated_at" : "2016-12-01T11:20:27.714-07:00",
      "reusable" : true,
      "data" : {
         "amount" : null,
         "guest" : "0",
         "sms_number" : null,
         "buyer_data" : "{\"billing\":{\"street\":\"123 Street Rd. NW\",\"street2\":\"\",\"city\":\"Albuquerque\",\"state\":\"NM\",\"zip\":\"87105\",\"phone\":\"\"},\"shipping\":null}",
         "email_opt_in" : "0"
      },
      "redacted_at" : null,
      "email_opt_in" : false,
      "atpay_token" : "YmI2ZjYyMWQ2Y1hAaeuMpQA=",
      "third_party_token" : null,
      "created_at" : "2016-12-01T11:20:27.300-07:00",
      "expiration_date" : "2022-01-01",
      "country" : "",
      "sms_number" : null,
      "card_mask" : "1111",
      "city" : "Albuquerque",
      "successful" : true,
      "phone" : "",
      "street" : "123 Street Rd. NW",
      "state" : "NM",
      "email" : "demo@example.com",
      "auth_token" : "9v1NaNwgE5TYpoM6GV9O7YI84TP",
      "street2" : "",
      "id" : 98,
      "card_type" : "visa",
      "last_name" : "Doe",
      "transaction_errors" : null,
      "zip" : "87105"
   }
  ]
{% endhighlight %}
