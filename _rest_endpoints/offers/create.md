---
title: Create an Offer
resource: offers
description: Creates a new Offer record.
type: POST
endpoint: https://api.atpay.com/api/v5/rest/offers
arguments:
    - name: demo
      description: Assigns to demo gateway.
      data_type: string
    - name: pcp_url_only
      description: will only return PCP link
      data_type: string
    - name: amount
      description: Dollar value of offer
      data_type: string
      required: true
layout: api_doc
---

## Example Request
{% highlight bash %}
curl https://api.atpay.com/api/v5/rest/offers \
  -u key:secret \
  -d demo=1 \
  -d amount=100
{% endhighlight %}

## Example Response
{% highlight json %}
{
   "offer" : {
      "title" : "Payment of $100.00.",
      "pcp_url" : "https://localhost:5000/offers/3D25EE85-0908-4EA6-A5A8-544A62ED9A45?",
      "details" : null,
      "created_at" : "2017-02-27T19:07:33.006-07:00",
      "offer_id" : "3D25EE85-0908-4EA6-A5A8-544A62ED9A45",
      "mail_to" : "mailto:payment-id-3D25EE85-0908-4EA6-A5A8-544A62ED9A45@ebfb85f1.ngrok.io?subject=Press%20send%20to%20give%20$100.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$100.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A",
      "button" : {
         "options" : {
            "wrap" : false,
            "image" : "https://www.atpay.com/wp-content/themes/atpay/images/bttn_cart.png",
            "wrap_text" : "Made for Mobile",
            "is_non_profit" : true,
            "templates" : "/Users/isaiah/.rbenv/versions/2.3.1/lib/ruby/gems/2.3.0/bundler/gems/atpay_ruby-792ccefdc017/lib/atpay/../../assets/button/templates",
            "locale" : "en",
            "foreground_color" : "#ffffff",
            "background_color" : "#6dbe45",
            "subject" : "Email Order Form",
            "title" : "Pay",
            "processor" : "ebfb85f1.ngrok.io",
            "analytic_url" : null
         },
         "locale" : "en",
         "amount" : 100,
         "merchant_name" : "@Pay NPO",
         "short_token" : "3D25EE85-0908-4EA6-A5A8-544A62ED9A45",
         "is_non_profit" : true,
         "token" : "at://3D25EE85-0908-4EA6-A5A8-544A62ED9A45"
      },
      "merchant" : "m_-hnOo_Ef_3KWw6juVeiPGw",
      "ref_id" : null,
      "amount" : 100,
      "button_html" : " <!— begin @Pay button —>\n\n<style>\n  .ExternalClass table.reg_mailto {display:none; display: none !important;}\n\n  .ExternalClass table.out_mailto {display: table; display: table !important; font-size: 18px !important; width: auto !important; height: auto !important;}\n  .ExternalClass table.out_mailto  {font-family: Tahoma; color: #ffffff;  background-color:#6dbe45;}\n\n  .ExternalClass table.out_mailto td.dollar{vertical-align:top !important; padding-right:0px !important; font-size:24px !important;  padding-top:15px !important;  text-align:right !important; padding-bottom:10px !important; padding-left:10px;}\n\n  .ExternalClass table.out_mailto td.cents{vertical-align:top !important; font-size:12px !important; padding-left:1px !important; padding-right:10px !important;  padding-bottom:0px !important; padding-top:15px !important; text-align:left !important; text-decoration:underline !important;}\n\n  .ExternalClass table.out_mailto  td img {display: block !important; height: 32px !important; width: 39px !important;}\n\n  .ExternalClass table.out_mailto  td.cart{width:45px !important; padding-left:10px !important; height:39px !important; text-align:right}\n\n  .ExternalClass table.out_mailto a {display: inline !important; border: 0 !important; width:auto !important; text-decoration:none !important; color:#ffffff !important; line-height:auto !important;}\n</style>\n\n<center>\n    \n\n    <table class=\"reg_mailto\" border='0' cellpadding='0' cellspacing='0' style='font-family: Tahoma; margin: 0 auto !important;  background-color:#6dbe45;'>\n      <tr>\n        \n          <td style=\"padding-left:10px; padding-right:0px; padding-top:14px; padding-bottom:10px;text-align:right;\">\n             <a class=\"reg_mailto\" href=\"mailto:payment-id-3D25EE85-0908-4EA6-A5A8-544A62ED9A45@ebfb85f1.ngrok.io?subject=Press%20send%20to%20give%20$100.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$100.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A\" target=\"_blank\" style=\"border-width: 0px;\">\n                <img src=\"https://www.atpay.com/wp-content/themes/atpay/images/bttn_cart.png\" style=\"display:block; border-width: 0px;\" />\n             </a>\n          </td>\n        \n            <td style=\"vertical-align:top; padding-left:10px; padding-right:0px; font-size:24px;  padding-top:15px;  text-align:right; padding-bottom:10px;\" valign=\"top\">\n               <a class=\"reg_mailto\" href=\"mailto:payment-id-3D25EE85-0908-4EA6-A5A8-544A62ED9A45@ebfb85f1.ngrok.io?subject=Press%20send%20to%20give%20$100.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$100.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A\" style=\"display: inline; width:auto;  border-width: 0px; line-height:auto; text-decoration:none; color: #ffffff;\" target=\"_blank\">\n               $100\n\n               </a>\n            </td>\n\n            <td class=\"cents\" style=\"vertical-align:top; font-size:12px; padding-left:1px; padding-right:10px;  padding-bottom:0px; padding-top:15px; text-align:left; text-decoration:none;\" valign=\"top\">\n               <a class=\"reg_mailto\" href=\"mailto:payment-id-3D25EE85-0908-4EA6-A5A8-544A62ED9A45@ebfb85f1.ngrok.io?subject=Press%20send%20to%20give%20$100.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$100.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A\" style=\"display: inline; border: 0 !important; width:auto; text-decoration:none !important; color:#ffffff; line-height:auto;\"  valign=\"top\" target=\"_blank\">.00</a>\n            </td>\n\n      </tr>\n    </table>\n\n    <table class='out_mailto'  border='0' cellpadding='0' cellspacing='0' style='width:0; height:0; padding:0; margin:0; font-size:0;'>\n      <tr>\n        \n          <td class='cart'>\n              <a href='https://www.hotmail.com/secure/start?action=compose&to=payment-id-3D25EE85-0908-4EA6-A5A8-544A62ED9A45@ebfb85f1.ngrok.io&subject=Press%20send%20to%20give%20$100.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$100.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A' style='display:none; border-width: 0px;'  target=\"_blank\">\n              <img src='https://www.atpay.com/wp-content/themes/atpay/images/bttn_cart.png' style='margin: 0px; width:0px; height:0px;  border-width: 0px;'>\n              </a>\n          </td>\n        \n        <td class='dollar' style='width:0; height:0; padding:0; margin:0; font-size:0;' valign='top'>\n          <a href='https://www.hotmail.com/secure/start?action=compose&to=payment-id-3D25EE85-0908-4EA6-A5A8-544A62ED9A45@ebfb85f1.ngrok.io&subject=Press%20send%20to%20give%20$100.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$100.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A' style='display:none; border-width: 0px;'  target=\"_blank\">\n            $100\n          </a>\n        </td>\n        <td class='cents' style='width:0; height:0; padding:0; margin:0; font-size:0;' valign='top'>\n        <a href='https://www.hotmail.com/secure/start?action=compose&to=payment-id-3D25EE85-0908-4EA6-A5A8-544A62ED9A45@ebfb85f1.ngrok.io&subject=Press%20send%20to%20give%20$100.00%20to%20@Pay%20NPO%20&body=@Pay%20NPO%20makes%20it%20easy%20to%20give.%20Simply%20press%20%22send%22%20to%20confirm%20your%20donation%20of%20$100.00.%20If%20we%20need%20more%20info,%20we%20will%20let%20you%20know.%20Thanks!%0A%0APowered%20by%20@Pay%0A' style='display:none; border-width: 0px;'  target=\"_blank\">\n          .00\n        </a>\n        </td>\n      </tr>\n    </table>\n</center>\n\n\n <!— end @Pay button —>\n"
   }
}
{% endhighlight %}
