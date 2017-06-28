---
title: Transaction Web Hook
description: Hook sent when a successful transaction occurs.
layout: hook_doc
---

## Example Hook
{% highlight json %}
{
  details : 
  {
    "confirmation_token" : null,
    "type" : "success",
    "transaction" : "D8113F50-DA24-403C-8234-284BE8107B0D",
    "merchant" : "m_GqOwzf8_eEVB4eS7uXUC0A",
    "amount" : "11.0",
    "date" : 1498678145,
    "card" : "NTAxNTc2MWQzZFlMEyGMpQA=",
    "payment_method" : "NTAxNTc2MWQzZFlMEyGMpQA=",
    "payment_method_mask" : "1111",
    "email" : "demo@example.com",
    "name" : "John Doe",
    "first_name" : "John", 
    "last_name" : "Doe",
    "user_data" : 
    {
      "custom_data" : {},
      "merchant_id" : "m_GqOwzf8_eEVB4eS7uXUC0A",
      "amount" : "11.00", 
      "invoice_number" : "1001",
      "shipping" : null,
      "billing" : 
      {
        "street" : "123 Street Rd. NW",
        "street2" : "",
        "city" : "Albuquerque",
        "state" : "NM",
        "zip" : "87105",
        "phone" : ""
        }
    },
    "referrer_context" : null, 
    "error" : null,
    "errors" : {},
    "recurring" : false,
    "processor" : "email",
    "source" : "Email Transaction",
    "token" : 
    {
      "user_data" : 
      {
        "custom_data" : {},
        "merchant_id" : "m_GqOwzf8_eEVB4eS7uXUC0A",
        "amount" : "11.00",
        "invoice_number" : "1001"
      },
      "active" : true,
      "amount" : 11.0,
      "url" : "https://localhost:5000/offers/F9E9E11C-89C6-4D6D-B49D-09217AE93948?email=demo%40example.com\u0026id=F9E9E11C-89C6-4D6D-B49D-09217AE93948",
      "signup_id" : "F9E9E11C-89C6-4D6D-B49D-09217AE93948"
    },
    "sms_info" : {}
  }
  signature: f4e7330899b505bbdba2315e9d5b9f695e4aecc7
}
{% endhighlight %}
