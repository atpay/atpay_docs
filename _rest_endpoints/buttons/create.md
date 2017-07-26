---
title: Create Buttons
resource: buttons
description: Creates buttons.
type: POST
endpoint: https://api.atpay.com/api/v5/rest/offers
arguments:
    - name: merchant_id
      description: Your account ID
      data_type: string
      required: true
    - name: authentication_only
      description: Always set to 'true'
      data_type: string
      required: true
headers:
    - key: Content-Type
      value: application/json
layout: api_doc
---

## Body
The body consists of an array of one or more JSON objects (described below) each corresponding to an individual button to be created.

### JSON Object

<table>
  <tr>
    <th>Key</th>
    <th>Description</th>
    <th>Required</th>
  </tr>
  <tr>
    <td>email</td>
    <td>If supplied, authentication requests using this button will only succeed if they come from the specified email address.</td>
    <td>false</td>
  </tr>
  <tr>
    <td>$CUSTOM</td>
    <td>Arbitrary custom arguments (e.g. "invoice_number") can be included, and they will returned with any associated web hook.</td>
    <td>false</td>
  </tr>  
</table>

## Example Request
{% highlight bash %}
curl -u key:secret \ 
  -X POST \
  -H "Content-Type: application/json" \
  -d '[{"email":"patrickw@atpay", "invoice_number":"1001"}]' \
  "https://api.atpay.com/api/v5/rest/offers?merchant_id=m_hOtXcnvLOGmjJt6kdU10aQ&authentication_only=true"
{% endhighlight %}

## Example Response
{% highlight json %}
[
  {
    "mailto": "mailto:payment-id-D175BAC7-0AE9-42FA-B362-ADC4D8FC3C4A@ebfb85f1.ngrok.io",
    "email": "patrickw@atpay",
    "invoice_number": "1001",
    "button_html": " <!— begin @Pay button —>\n\n<style>\n  .ExternalClass table.reg_mailto {display:none; display: none !important;}\n\n  .ExternalClass table.out_mailto {display: table; display: table !important; font-size: 18px !important; width: auto !important; height: auto !important;}\n  .ExternalClass table.out_mailto  {font-family: Tahoma; color: #ffffff;  background-color:#6dbe45;}\n\n  .ExternalClass table.out_mailto td.dollar{vertical-align:top !important; padding-right:0px !important; font-size:24px !important;  padding-top:15px !important;  text-align:right !important; padding-bottom:10px !important; padding-left:10px;}\n\n  .ExternalClass table.out_mailto td.cents{vertical-align:top !important; font-size:12px !important; padding-left:1px !important; padding-right:10px !important;  padding-bottom:0px !important; padding-top:15px !important; text-align:left !important; text-decoration:underline !important;}\n\n  .ExternalClass table.out_mailto  td img {display: block !important; height: 32px !important; width: 39px !important;}\n\n  .ExternalClass table.out_mailto  td.cart{width:45px !important; padding-left:10px !important; height:39px !important; text-align:right}\n\n  .ExternalClass table.out_mailto a {display: inline !important; border: 0 !important; width:auto !important; text-decoration:none !important; color:#ffffff !important; line-height:auto !important;}\n</style>\n\n<center>\n    \n\n    <table class=\"reg_mailto\" border='0' cellpadding='0' cellspacing='0' style='font-family: Tahoma; margin: 0 auto !important;  background-color:#6dbe45;'>\n      <tr>\n        \n          <td style=\"padding-left:10px; padding-right:0px; padding-top:14px; padding-bottom:10px;text-align:right;\">\n             <a class=\"reg_mailto\" href=\"mailto:payment-id-D175BAC7-0AE9-42FA-B362-ADC4D8FC3C4A@ebfb85f1.ngrok.io?subject=Press%20send%20to%20give%20$0.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$0.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A\" target=\"_blank\" style=\"border-width: 0px;\">\n                <img src=\"https://www.atpay.com/wp-content/themes/atpay/images/bttn_cart.png\" style=\"display:block; border-width: 0px;\" />\n             </a>\n          </td>\n        \n            <td style=\"vertical-align:top; padding-left:10px; padding-right:0px; font-size:24px;  padding-top:15px;  text-align:right; padding-bottom:10px;\" valign=\"top\">\n               <a class=\"reg_mailto\" href=\"mailto:payment-id-D175BAC7-0AE9-42FA-B362-ADC4D8FC3C4A@ebfb85f1.ngrok.io?subject=Press%20send%20to%20give%20$0.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$0.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A\" style=\"display: inline; width:auto;  border-width: 0px; line-height:auto; text-decoration:none; color: #ffffff;\" target=\"_blank\">\n               $0\n\n               </a>\n            </td>\n\n            <td class=\"cents\" style=\"vertical-align:top; font-size:12px; padding-left:1px; padding-right:10px;  padding-bottom:0px; padding-top:15px; text-align:left; text-decoration:none;\" valign=\"top\">\n               <a class=\"reg_mailto\" href=\"mailto:payment-id-D175BAC7-0AE9-42FA-B362-ADC4D8FC3C4A@ebfb85f1.ngrok.io?subject=Press%20send%20to%20give%20$0.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$0.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A\" style=\"display: inline; border: 0 !important; width:auto; text-decoration:none !important; color:#ffffff; line-height:auto;\"  valign=\"top\" target=\"_blank\">.00</a>\n            </td>\n\n      </tr>\n    </table>\n\n    <table class='out_mailto'  border='0' cellpadding='0' cellspacing='0' style='width:0; height:0; padding:0; margin:0; font-size:0;'>\n      <tr>\n        \n          <td class='cart'>\n              <a href='https://www.hotmail.com/secure/start?action=compose&to=payment-id-D175BAC7-0AE9-42FA-B362-ADC4D8FC3C4A@ebfb85f1.ngrok.io&subject=Press%20send%20to%20give%20$0.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$0.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A' style='display:none; border-width: 0px;'  target=\"_blank\">\n              <img src='https://www.atpay.com/wp-content/themes/atpay/images/bttn_cart.png' style='margin: 0px; width:0px; height:0px;  border-width: 0px;'>\n              </a>\n          </td>\n        \n        <td class='dollar' style='width:0; height:0; padding:0; margin:0; font-size:0;' valign='top'>\n          <a href='https://www.hotmail.com/secure/start?action=compose&to=payment-id-D175BAC7-0AE9-42FA-B362-ADC4D8FC3C4A@ebfb85f1.ngrok.io&subject=Press%20send%20to%20give%20$0.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$0.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A' style='display:none; border-width: 0px;'  target=\"_blank\">\n            $0\n          </a>\n        </td>\n        <td class='cents' style='width:0; height:0; padding:0; margin:0; font-size:0;' valign='top'>\n        <a href='https://www.hotmail.com/secure/start?action=compose&to=payment-id-D175BAC7-0AE9-42FA-B362-ADC4D8FC3C4A@ebfb85f1.ngrok.io&subject=Press%20send%20to%20give%20$0.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$0.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A' style='display:none; border-width: 0px;'  target=\"_blank\">\n          .00\n        </a>\n        </td>\n      </tr>\n    </table>\n</center>\n\n\n <!— end @Pay button —>\n"
  }
]
{% endhighlight %}
