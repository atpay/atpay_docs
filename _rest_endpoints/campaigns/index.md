---
title: List all Campaigns
resource: campaigns
description: List all Campaigns associate with a given Organization
type: GET
endpoint: https://app.atpay.com/api/v5/campaigns
arguments:
    - name: merchant_id
      description: Merchant ID of the Organization to which the campaign belongs.
      data_type: string
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://app.atpay.com/api/v5/campaigns \
  -u key:secret \
  -d merchant_id=m_XXXXXXXXXXXXXXXXXXXXXX
{% endhighlight %}

## Example Response
{% highlight json %}
[
  {
    "id": 24,
    "organization_id": 24,
    "slug": "default-campaign",
    "title": "Default Campaign",
    "header": null,
    "description": null,
    "goal": null,
    "default": true,
    "created_at": "2017-07-10T19:34:54.713Z",
    "updated_at": "2017-07-10T19:34:54.713Z",
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
  },
  {
    "id": 34,
    "organization_id": 24,
    "slug": "title-1",
    "title": "Title 1",
    "header": null,
    "description": null,
    "goal": null,
    "default": null,
    "created_at": "2017-07-10T21:08:07.719Z",
    "updated_at": "2017-07-10T21:08:07.719Z",
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
  },
  {
    "id": 35,
    "organization_id": 24,
    "slug": "title-2",
    "title": "Title 2",
    "header": null,
    "description": null,
    "goal": null,
    "default": null,
    "created_at": "2017-07-10T21:09:53.719Z",
    "updated_at": "2017-07-10T21:09:53.719Z",
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
  },
  {
    "id": 44,
    "organization_id": 24,
    "slug": "title-2-2",
    "title": "Title 2",
    "header": null,
    "description": null,
    "goal": null,
    "default": null,
    "created_at": "2017-07-27T21:05:33.222Z",
    "updated_at": "2017-07-27T21:05:33.222Z",
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
  },
  {
    "id": 45,
    "organization_id": 24,
    "slug": "title-2-3",
    "title": "Title 2",
    "header": null,
    "description": null,
    "goal": null,
    "default": null,
    "created_at": "2017-07-27T21:08:31.421Z",
    "updated_at": "2017-07-27T21:08:31.421Z",
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
  },
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
]
{% endhighlight %}