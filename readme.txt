=== PMPro Sponsored Members ===
Contributors: strangerstudios
Tags: pmpro, membership, user pages
Requires at least: 3.0
Tested up to: 3.5.2
Stable tag: .1

Generate a discount code for a main account holder to distribute to sponsored members.

== Description ==

This plugin currently requires Paid Memberships Pro. 

This plugin is meant as a functional demo on how to implement sponsored memberships with Paid Memberships Pro. Feel free to edit as needed for your project.

Once the plugin is activated with the PMPROSM_MAIN_ACCOUNT_LEVEL and PMPROSM_SPONSORED_ACCOUNT_LEVEL, your site will:
* When users checkout for a main account (or are assigned one by and admin), a discount code is generated to allow sponsored members to sign up for the sponsored level for free.
* If a user has a discount code assigned to them, it will show up on their membership account and confirmation pages.
* Only members using a sponsored discount code will be able to sign up for the sponsored level.
* Sponsored members will be linked to their sponsor through the pmpro_discount_codes_uses table.
* If a sponsor's account is cancelled, all of their sponsored members will have their accounts disabled as well.
* If a sponsor's account is enabeld later (a user with an existint discount code checking, etc), all of their sponsored members will have their accounts enabled

== Installation ==

1. Upload the `pmpro-sponsored-members` directory to the `/wp-content/plugins/` directory of your site.
1. Activate the plugin through the 'Plugins' menu in WordPress.
1. Create one level for paying account holders and one level for sponsored members.
1. Edit the PMPROSM_MAIN_ACCOUNT_LEVEL constant in the plugin file to match your main account level id.
1. Edit the PMPROSM_SPONSORED_ACCOUNT_LEVEL constant in the plugin file to match your sponsored level id.
1. Edit the second half of the pmprosm_pmpro_after_change_membership_level() function to change the values of the discount code given to paying members.

== Frequently Asked Questions ==

= I found a bug in the plugin. =

Please post it in the issues section of GitHub and we'll fix it as soon as we can. Thanks for helping. https://github.com/strangerstudios/pmpro-sponsored-members/issues

== Changelog ==

= .1 =
* This is the initial version of the plugin.