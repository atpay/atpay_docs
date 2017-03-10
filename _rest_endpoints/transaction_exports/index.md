---
title: List Transactions
resource: null
description: Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
type: GET
endpoint: https://api.atpay.com/api/v5/rest/transactions
arguments:
    - name: name
      description: description
      data_type: string
      optional: true
    - name: name
      description: description
      data_type: string
      optional: true
    - name: name
      description: description
      data_type: string
      optional: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.stripe.com/v1/balance/history?limit=3 \
   -u sk_test_UZT8TxB5GSaYukclrTFbffRY: \
   -G
{% endhighlight %}

## Example Response
{% highlight json %}
{
  "id": "evt_19rjVX2cyTQBFAI5cj9SbGu6",
  "object": "event",
  "api_version": "2015-10-16",
  "created": 1488182723,
  "data": {
    "object": {
      "id": "tr_19rjVW2cyTQBFAI5g9q04zW0",
      "object": "transfer",
      "amount": 4740,
      "amount_reversed": 0,
      "application_fee": null,
      "balance_transaction": "txn_19rjVW2cyTQBFAI5YzHpKlWJ",
      "bank_account": {
        "id": "ba_103Znk2cyTQBFAI5PM0s2AZv",
        "object": "bank_account",
        "account_holder_name": null,
        "account_holder_type": null,
        "bank_name": "NEW MEXICO BANK \u0026 TRUST",
        "country": "US",
        "currency": "usd",
        "fingerprint": null,
        "last4": "2108",
        "routing_number": "107006541",
        "status": "new",
        "name": null
      },
      "created": 1488182722,
      "currency": "usd",
      "date": 1488240000,
      "description": "STRIPE TRANSFER",
      "destination": "ba_103Znk2cyTQBFAI5PM0s2AZv",
      "failure_code": null,
      "failure_message": null,
      "livemode": false,
      "metadata": {
      },
      "method": "standard",
      "recipient": null,
      "reversals": {
        "object": "list",
        "data": [
        ],
        "has_more": false,
        "total_count": 0,
        "url": "/v1/transfers/tr_19rjVW2cyTQBFAI5g9q04zW0/reversals"
      },
      "reversed": false,
      "source_transaction": null,
      "source_type": "card",
      "statement_descriptor": null,
      "status": "in_transit",
      "transfer_group": null,
      "type": "bank_account"
    }
  },
  "livemode": false,
  "pending_webhooks": 0,
  "request": null,
  "type": "transfer.created"
}
{% endhighlight %}
