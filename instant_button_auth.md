---
layout: auth
---
# How Instant Buttons Work On Your Site
{: style="text-align: center"}

![Instant Button Authentication flow diagram]({{ "/assets/img/diagram.jpg" | relative_url }})
{: style="text-align: center"}

### You or your developers will need to create an app that does the following: 

1. Your App POSTS dollar amount, email address, and a unique customer ID to @Pay. 
2. Your App receives the HTML/CSS code for an Instant Button for display on your site or email campaign. 
3. When a custom selects the Instant Pay/Instant Buy option, the payment email will enter out authentication service for authorization. 
4. Your App will need to be able to receive our web hooks indicating either a successful or unsuccessful authentication. 
5. Successful authentication should trigger completion of the payment process through your already existing services. 