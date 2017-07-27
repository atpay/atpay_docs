---
title: Show an Organization
resource: organizations
description: Shows details about a given organization.
type: GET
endpoint: https://app.atpay.com/api/v5/organizations/0
arguments:
    - name: ref
      description: Should always be 'sid'. It defines how we look up the organization.
      data_type: string
      required: true
    - name: merchant_id
      description: The merchant ID of the Organization you'd like to look up.
      data_type: string
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://app.atpay.com/api/v5/organizations \
  -u key:secret \
  -d ref="sid" \
  -d merchant_id="m_v2Uutovjqb4OCGp-s2RQPA" \
{% endhighlight %}

## Example Response
{% highlight json %}
{
  "config": {
    "merchant_id": "m_v2Uutovjqb4OCGp-s2RQPA",
    "default_gateway": "gw_AutrJ4aYhDFX1SBzYRHmeQ",
    "test_gateway": "gw_AutrJ4aYhDFX1SBzYRHmeQ"
  },
  "organization": {
    "id": 30,
    "organization_id": 30,
    "name": "Test 13",
    "dba": null,
    "slug": "test-13",
    "contact_name": null,
    "contact_email": "test@example.com",
    "contact_phone": null,
    "address": null,
    "state": null,
    "city": null,
    "zip": null,
    "custom_messaging": null,
    "minimum_transaction_amount": null,
    "transaction_notification": null,
    "created_at": "2017-07-27T20:30:45.029Z",
    "updated_at": "2017-07-27T20:30:45.029Z",
    "sms_number": null
  },
  "theme": {
    "color_scheme": {
      "primary_background_color": "#00022e",
      "secondary_background_color": "#1280a8",
      "primary_text_color": "#ffffff",
      "secondary_text_color": "#0077b7"
    },
    "logo": null,
    "background_image": null,
    "organization_logo": null
  }
}
{% endhighlight %}