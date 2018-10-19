# shopify-tracking-info-notification
  Add tracking number, tracking URLs to Notification emails on Shopify
--------
If you want to add tracking number to the notification html email, you can open Shipping confirmation templates and edit by yourself.

You can follow these steps by clicking this [link](https://ecommerce.shopify.com/c/shopify-discussion/t/how-to-add-the-tracking-id-to-the-shipping-confirmation-notification-401182).

Also you can view the documentation by clicking this [Link](https://help.shopify.com/en/manual/sell-online/notifications/email-variables#fulfillment-properties) .

----------        

### Basic steps:
* fulfillment.tracking_company
* fulfillment.tracking_numbers
* fulfillment.tracking_urls

Choose the code you want, then insert to the shipping confirmation email. Looks like this:


      <h2>{{ email_title }}</h2>
      <p>{{ email_body }}</p>
      {% if fulfillment.estimated_delivery_at %}
      <p>{{ email_emphasis }}</p>
      {% endif %}
      {% if order_status_url %}
       <p>Tracking number is <a href="{{ fulfillment.tracking_urls }}">{{ fulfillment.tracking_numbers }}</a> </p>
       
       
Then the tracking number and the link will be sent to your customers.       
       
       




