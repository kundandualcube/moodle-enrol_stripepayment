Moodle Stripe Enrollment Plugin [enrol_stripepayment]
=======================
* Developed by: Team DualCube
* Copyright: (c) 2023 DualCube <admin@dulacube.com>
* License: [GNU GENERAL PUBLIC LICENSE](LICENSE)
* Contributors:  DualCube

Description
===========
This plugin helps admins and webmasters use Stripe as the payment gateway. Stripe is one of the popular payment gateways. This plugin has all the settings for development as well as for production usage. It is easy to install, setup and effective.

_Added features include:_
* Complerely SCA Compatible
* Coupon functionality while enrolling students with percent-off or amount-off discount
* Full course name and site logo on stripe checkout
* Ability to set custom stripe transaction statement descriptor for each course
* Admins and Webmasters, now, can create, manage, and keep track of all promotional codes directly in their Stripe dashboard.

Installation
============
1. Login to your moodle site as an “admin user” and follow the steps.
2. Upload the zip package from Site administration > Plugins > Install plugins. Choose Plugin type 'Enrolment method (enrol)'. Upload the ZIP package, check the acknowledgement and install.
3. Go to Enrolments > Manage enrol plugins > Enable 'Stripe' from list
4. Click 'Settings' which will lead to the settings page of the plugin
5. Provide merchant credentials for Stripe. Note that, you will get all the details from your merchant account. For User Token follow next stap. Now select the checkbox as per requirement. Save the settings.
6. Access Token: Site Administration > Server tab > Web Services > Manage Tokens. select Create Token. [User – Admin, Service – moodle_enrol_stripepayment]. Copy Token ID to Stripe Settings on above stap.
7. Enable Web Service: Administration > Development Section > Advanced Features option. scroll down and tick the Web Service option, and save.
8. Manage Protocol: Site Administration > Server tab > Web Services > Manage Protocols. Click on the eye icon on the REST protocol, and save.
9. Select any course from course listing page.
10. Go to Course administration > Participants > Enrolment methods > Add method 'Stripe' from the dropdown. Set 'Custom instance name', 'Enrol cost', 'Currency' etc and add the method.
11. This completes all the steps from the administrator end. Now registered users can login to the Moodle site and view the course after a successful payment.

[Note: If you missed step no. 7 & 8 - it will give error-403 on payment page ]

Adding Coupons
==============
1. Go to your Stripe Dashboard >  Product > Coupons > Create a coupon.
2. Type in the coupon’s name: it can be anything and for your reference only.
  Type in the Coupon’s ID: This is the Coupon code that your students will need to enter if they want to avail of the discount.

  Choose Coupon Type: 
    1. Percentage discount: offers % off on the course price 
    2. Fixed amount discount: Offers a fixed amount off on the course price.

  Duration: For the duration, when using the value repeating, also specify the duration in months as the number of months for which the coupon should repeatedly apply. Otherwise, the coupon can be set to apply only to a single invoice or to them all.

Redemption: The max_redemptions and redeem_by values apply to the coupon across every customer you have. For example, you can restrict a coupon to the first 50 customers that use it, or you can make a coupon expire by a certain date. If you do the latter, this only impacts when the coupon can be applied to a customer. 
If you set a coupon to last forever when used by a customer, but have it expire on January 1st, any customer is given that coupon will have that coupon’s discount forever, but no new customers can apply the coupon after January 1st.

If a coupon has a max_redemptions value of 50, it can only be applied among all your customers a total of 50 times, although there’s nothing preventing a single customer from using it multiple times. (You can always use logic on your end to prevent that from occurring.)

This completes all the steps from the administrator end. Now registered users can log in to the Moodle site and view the course after successful payment of the discounted price.

Requirements
------------
* Moodle 3.9.x - 4.3.x
* Stripe account


How to create Stripe account
--------------
1. Create account at https://stripe.com.
2. Complete your merchant profile details from https://dashboard.stripe.com/account.
3. Now set up secret key and publishers key at https://dashboard.stripe.com/account/apikeys.
4. For test mode use test api keys and for live mode use live api keys.
5. Now you are done with merchant account set up.


Useful links
============
* Moodle Forum: [https://moodle.org/course](https://moodle.org/course)
* Moodle Plugins Directory:  [https://moodle.org/plugins](https://moodle.org/plugins)
* Stripe API: [https://stripe.com/docs/api?lang=php#intro](https://stripe.com/docs/api?lang=php#intro)
* DualCube Contributions: [https://moodle.org/plugins/browse.php?list=contributor&id=1832609](https://moodle.org/plugins/browse.php?list=contributor&id=1832609)


Release history
===============
* **v1.0:** 2016-05-05
