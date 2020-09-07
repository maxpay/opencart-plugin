Maxpay payment module for Opencart 3.0 or higher.

### Installation

* Backup your webstore and database
* Upload the module file maxpay.ocmod.zip via _Extensions_ -> _Extension Installer_
* Activate the module in payment extensions (_Extensions_ -> _Payments_)
* Configure the module settings:
    * Public key
    * Private key
    * Enabled the module
    * Test mode
    * Public test key
    * Private test key
    * Configure order statuses for successfuly processed payment and for failed, refaund, pending

### Notes

Tested and developed with OpenCart v.3.0.3.2, PHP 7.2

### General setup:
1. Login/register to https://my.maxpay.com
2. Create Payment page and get Public/Private keys (test keys are also available here).
3. Use these keys to configure Maxpay payment module.
4. On module configuration page you can enable Test mode if neccessary.
5. All the other settings are done in Maxpay control panel (https://my.maxpay.com). 
There you can specify success/decline/callback urls for test/prod mode.

### Recommendations are:

Success url: {{YOUR_SITE_URL}}/index.php?route=extension/payment/maxpay/accept  
Decline url: {{YOUR_SITE_URL}}/index.php?route=extension/payment/maxpay/cancel  
Callback url: {{YOUR_SITE_URL}}/index.php?route=extension/payment/maxpay/callback

{{YOUR_SITE_URL}} - your site url (e.g. https://maxpay.com)

### USAGE
Payment processing is done by redirecting the Customer to Maxpay payment page. 
All the payment settings are done in Maxpay Control Panel (https://my.maxpay.com).

### REFUND FUNCTIONALITY
To refund an order you just need to change the status of the order to Refund. 
This event will trigger Maxpay to handle money refund on this order, if payment has been done using Maxpay payment method.

Partial reefund is not yet implemented by this module.
