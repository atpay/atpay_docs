---
title: Retrieve a Credit Card
resource: credit-cards
description: Retrieves specific Credit Card object record
type: GET
endpoint: "https://api.atpay.com/api/v5/rest/credit_cards/{atpay_token}"
arguments:
    - name: atpay_token
      description: '@Pay Payment Token'
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/rest/credit_cards/OTBjMmVhMDBmNVhAlHuMpQA= -u key:secret
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "street" : "123 Street Rd. NW",
   "redacted_at" : null,
   "created_at" : "2016-12-01T14:22:03.055-07:00",
   "one_time_use" : false,
   "card_mask" : "1881",
   "third_party_token" : null,
   "email_opt_in" : false,
   "phone" : "",
   "updated_at" : "2016-12-01T14:22:03.494-07:00",
   "country" : "",
   "data" : {
      "amount" : null,
      "buyer_data" : "{\"billing\":{\"street\":\"123 Street Rd. NW\",\"street2\":\"\",\"city\":\"Albuquerque\",\"state\":\"NM\",\"zip\":\"87105\",\"phone\":\"\"},\"shipping\":null}",
      "sms_number" : null,
      "guest" : "0",
      "email_opt_in" : "0"
   },
   "city" : "Albuquerque",
   "email" : "demo@example.com",
   "successful" : true,
   "transaction_errors" : null,
   "card_type" : "visa",
   "id" : 111,
   "expiration_date" : "2022-01-01",
   "sms_number" : null,
   "zip" : "87105",
   "reusable" : true,
   "first_name" : "John",
   "state" : "NM",
   "street2" : "",
   "auth_token" : "SRy3jPVeZtu08Bo09X8Auyl5Jvx",
   "atpay_token" : "OTBjMmVhMDBmNVhAlHuMpQA=",
   "last_name" : "Doe"
}
{% endhighlight %}
