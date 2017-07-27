---
title: Show a Campaign
resource: campaigns
description: Shows details about a given campaign.
type: GET
endpoint: https://app.atpay.com/api/v5/campaigns/:campaign_slug
arguments:
    - name: merchant_id
      description: Merchant ID of the Organization to which the campaign belongs.
      data_type: string
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://app.atpay.com/api/v5/campaigns/title-2-4 \
  -u key:secret \
  -d merchant_id=m_XXXXXXXXXXXXXXXXXXXXXX
{% endhighlight %}

## Example Response
{% highlight json %}
{
  "id": 46,
  "organization_id": 24,
  "slug": "title-2-4",
  "title": "Title 2",
  "header": null,
  "description": null,
  "goal": null,
  "default": null,
  "created_at": "2017-07-27T21:10:52.353Z",
  "updated_at": "2017-07-27T21:10:52.353Z",
  "tags": [],
  "recurring": true,
  "custom_receipt_messaging": null,
  "hide_thermometer_instructions": true,
  "inclusive_fees_option": null,
  "theme": {
    "color_scheme": {
      "primary_background_color": "#00022e",
      "secondary_background_color": "#1280a8",
      "primary_text_color": "#ffffff",
      "secondary_text_color": "#0077b7",
      "email_background_color": "#0077b7",
      "link_color": "#0077b7"
    },
    "logo": null,
    "background_image": null,
    "organization_logo": null
  },
  "transaction_rate": 2.9
}
{% endhighlight %}