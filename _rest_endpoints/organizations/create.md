---
title: Create an Organization
resource: organizations
description: Creates a new Organization.
type: POST
endpoint: https://app.atpay.com/api/v5/organizations
arguments:
    - name: organization[details_attributes[name]]
      description: Name of the new Organization.
      data_type: string
      required: true
    - name: organization[users_attributes[0][email]]
      description: Email of the user to be created along with this Organization
      data_type: string
      required: true
    - name: organization[users_attributes[0][password]]
      description: Password of the user to be created along with this Organization
      data_type: string
      required: true
    - name: organization[organization_plan_attributes[partner]]
      description: Your merchant ID.
      data_type: string
      required: true
    - name: organization[organization_plan_attributes[plan_id]]
      description: ID of the Plan to associate with the new Organization.
      data_type: string
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://app.atpay.com/api/v5/organizations \
  -u key:secret \
  -d organization[details_attributes[name]]="My Test Organization" \
  -d organization[users_attributes[0][email]]=user@email.com \
  -d organization[users_attributes[0][password]]="supersecurepassword" \ 
  -d organization[organization_plan_attributes[partner]]=m_XXXXXXXXXXXXXXXXXXXXXX \
  -d organization[organization_plan_attributes[plan_id]]=1008
{% endhighlight %}

## Example Response
{% highlight json %}
{
  "giving_portal_url" : "https://my-test-organization.atpy.it",
  "merchant_id" : "m_XXXXXXXXXXXXXXXXXXXXXX"
}
{% endhighlight %}