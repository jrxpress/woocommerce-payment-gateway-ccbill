=== Plugin Name ===
Contributors: CCBill
Tags: CCBill, payment, gateway, WooCommerce
Requires at least: 3.0.1
Tested up to: 3.4
Stable tag: trunk
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Accept CCBill payments on your WooCommerce website.

== Description ==

The CCBill payment gateway plugin for WooCommerce allows you to easily configure and accept CCBill
payments on your WooCommerce-enabled Wordpress Website.

This plugin requires WooCommerce.

== Installation ==

Installation involves the following steps:
* Installing the CCBill payment module for WooCommerce
* Configuring your CCBill account for use with WooCommerce
* Configuring the module with your CCBill account information

**Installation Options**

The CCBill WooCommerce module can be installed either by searching for the hosted WordPress plugin, or by uploading the plugin downloaded from the CCBill website.

**Installing via WordPress Plugin Directory**

From the WordPress administration menu, navigate to “Plugins.”  
Type “CCBill” into the text field and click “Search Plugins.”  
Locate the official CCBill plugin for WooCommerce from the search 
results and click the “Install Now” link next to the module title.

**Installing via File Upload**

From the WordPress administration menu, navigate to "Plugins" 
and selected "Upload" from the top menu.  Click the "Choose File" 
button and select the .zip file downloaded from the CCBill website
or Wordpress plugin directory.
  
Once the file is selected, click "Install Now" to complete 
the installation process.

**Configuring your CCBill Account**

Before using the plugin, it’s necessary to configure a few things in your CCBill account.  
Please ensure the CCBill settings are correct, or the payment module will not work.

**Enabling Dynamic Pricing**

Please work with your CCBill support representative to activate "Dynamic Pricing" for your account.  
You can verify that dynamic pricing is active by selecting "Feature Summary" under the 
"Account Info" tab of your CCBill admin menu.  Dynamic pricing status appears at the 
bottom of the "Billing Tools" section.

**Creating a Salt / Encryption Key**

A "salt" is a string of random data used to make your encryption more secure.  
You must contact CCBill Support to generate your salt.  Once set, it will be 
visible under the "Advanced" section of the "Sub Account Admin" menu.  It will 
appear in the "Encryption Key" field of the "Upgrade Security Setup Information" 
section.

**Disabling User Management**

Since this account will be used for dynamic pricing transactions rather than 
managing user subscription, user management must be disabled.
In your CCBill admin interface, navigate to "Sub Account Admin" and select 
"User Management" from the left menu.  
Select "Turn off User Management" in the top section.  
Under "Username Settings," select "Do Not Collect Usernames and Passwords."

**Creating a New Billing Form**

The billing form is the CCBill form that will be displayed to customers after 
they choose to check out using CCBill.  The billing form accepts customer 
payment information, processes the payment, and returns the customer to your 
WooCommerce store where a confirmation message is displayed.

To create a billing form for use with WooCommerce, navigate to the "Form Admin" 
section of your CCBill admin interface.  All existing forms will be displayed 
in a table.

Click "Create New Form" in the left menu to create your new form.

Select the appropriate option under "Billing Type."  (In most cases, this will 
be "Credit Card.")

Select "Standard" under "Form Type" unless you intend to customize your form.

Select the desired layout, and click "Submit" at the bottom of the page.

Your new form has been created, and is visible in the table under "View All Forms."  
In this example, our new form is named "201cc."  Be sure to note the name of 
your new form, as it will be required in the WooCommerce configuration section.


**Configuring the New Billing Form**

Click the title of the newly-created form to edit it.  In the left menu, 
click "Basic."

Under "Basic," select an Approval Redirect Time of 3 seconds, and a 
Denial Redirect Time of "Instant."


**Configuring Your CCBill Account**

In your CCBill admin interface, navigate to "Sub Account Admin" and select "Basic" from the left menu.  
Site Name

Enter the URL of your WooCommerce store under "Site Name"

**Approval URL**

Under Approval URL, enter the base URL for your WooCommerce store, followed by: 
/?wc-api=WC_Gateway_CCBill&Action=CheckoutSuccess

For example, if your WooCommerce store is located at http://www.test.com, the Approval URL would be:
http://www.test.com/?wc-api=WC_Gateway_CCBill&Action=CheckoutSuccess

If your WooCommerce store is located at http://www.test.com/woo, then the Approval URL would be:
http://www.test.com/woo/?wc-api=WC_Gateway_CCBill&Action=CheckoutSuccess

**Denial URL**

Under Denial URL, enter the base URL for your WooCommerce store, followed by: 
/?wc-api=WC_Gateway_CCBill&Action=CheckoutFailure

For example, if your WooCommerce store is located at http://www.test.com, the Denial URL would be:
http://www.test.com/?wc-api=WC_Gateway_CCBill&Action=CheckoutFailure

If your WooCommerce store is located at http://www.test.com/woo, then the Denial URL would be:
http://www.test.com/woo/?wc-api=WC_Gateway_CCBill&Action=CheckoutFailure

**Redirect Time**

Select an approval redirect time of 3 seconds, and a denial redirect time of "Instant."

**Background Post**

While still in the “Sub Account Admin” section, select “Advanced” from the left menu.  Notice the top section titled “Background Post Information.”  We will be modifying the Approval Post URL and Denial Post URL fields.

**Approval Post URL**
Under Approval Post URL, enter the base URL for your WooCommerce store, followed by: 
/?wc-api=WC_Gateway_CCBill&Action=Approval_Post

For example, if your WooCommerce store is located at http://www.test.com, the Approval URL would be:
http://www.test.com//?wc-api=WC_Gateway_CCBill&Action=Approval_Post

If your WooCommerce store is located at http://www.test.com/woo, then the Approval URL would be:
http://www.test.com/woo//?wc-api=WC_Gateway_CCBill&Action=Approval_Post

**Denial Post URL**
Under Denial Post URL, enter the base URL for your WooCommerce store, followed by: 
/?wc-api=WC_Gateway_CCBill&Action=Denial_Post

For example, if your WooCommerce store is located at http://www.test.com, the Denial URL would be:
http://www.test.com/?wc-api=WC_Gateway_CCBill&Action=Denial_Post

If your WooCommerce store is located at http://www.test.com/woo, then the Denial URL would be:
http://www.test.com/woo/?wc-api=WC_Gateway_CCBill&Action=Denial_Post

**Confirmation**
Your CCBill account is now configured. In your CCBill admin interface, navigate to "Sub Account Admin" and ensure the information displayed is correct.


== Changelog ==

= 1.0 =
* Initial Release

