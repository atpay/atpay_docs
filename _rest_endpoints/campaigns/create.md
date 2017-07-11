---
title: Create a Campaign
resource: campaigns
description: Creates a new Campaign
type: POST
endpoint: https://api.atpay.com/api/v5/rest/campaigns
arguments:
    - name: merchant_id
      description: Merchant ID of the Organization on which to create the Campaign.
      data_type: string
      required: true
    - name: campaign[title]
      description: The title of the new Campaign. 
      data_type: string
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/campaigns \
  -u key:secret \
  -d merchant_id=m_XXXXXXXXXXXXXXXXXXXXXX \
  -d campaign[title]="Campaign Title"
{% endhighlight %}

## Example Response
{% highlight json %}
{
  "form_url" : "https://my-test-organization.atpy.it/campaign-title"
}
{% endhighlight %}