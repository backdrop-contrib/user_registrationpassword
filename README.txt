
CONTENTS OF THIS FILE
---------------------

 * Introduction
 * Installation
 * Configuration
 * Multilangual sites


INTRODUCTION
------------

Let users register with a password on the registration form when verification mail is required.

By default, users can create accounts directly on the registration form, set their password and
be immediately logged in, or they can create their account, wait for a verification e-mail, and
then create their password. With this module, users are able to create their account along with
their password and simply activate their account when receiving the verification email.


INSTALLATION
------------

Installation is like any other module, just place the files in the
sites/all/modules directory and enable the module on the modules page.


CONFIGURATION
-------------

On the admin/config/people/accounts page make sure you have selected:

Who can register accounts?
0 Administrators only
X Visitors
0 Visitors, but administrator approval is required

Then select 'Require a verification e-mail, but let users set their password directly on the registration form.' at:

Require e-mail verification when a visitor creates an account
0 Do not require a verification e-mail, and let users set their password on the registration form.
0 Require a verification e-mail, but wait for the approval e-mail to let users set their password.
X Require a verification e-mail, but let users set their password directly on the registration form.

You also have to change the 'Account Activation' welcome email template on the bottom of the same page.

By default, Drupal will send the following Email:

-----------------------------------------------------------------------------------------------------------------------

[user:name],

Your account at [site:name] has been activated.

You may now log in by clicking this link or copying and pasting it into your browser:

[user:one-time-login-url]

This link can only be used once to log in and will lead you to a page where you can set your password.

After setting your password, you will be able to log in at [site:login-url] in the future using:

username: [user:name]
password: Your password

--  [site:name] team

-----------------------------------------------------------------------------------------------------------------------

This will be confusing, because it also contains a login link, a link we do need anymore, because we already verified
the account, and the link will not work anyway. ( possible TODO ? )

The most simple way to fix this situation is to rewrite the template to look something like this:

-----------------------------------------------------------------------------------------------------------------------

[user:name],

Your account at [site:name] has been activated.

You may now log in by surfing to [site:login-url] with the username and password you used to register.

--  [site:name] team

-----------------------------------------------------------------------------------------------------------------------

That's all! The module is now configured correctly.


MULTILANGUAL SITES
------------------

For multilangual sites: i18n / variables are supported for the e-mail template.
Be sure to enable them at the admin/config/regional/i18n/variable page and to
translate them via the admin/config/regional/translate page.

Ones configured correctly, users will receive an e-mail in their default
language, setting available on user's edit page. It does not matter what the
site language is, this setting will be leading and overwrite the site's default
language. So it is logical and corrent that if you have an German based site
with, let's say German and English languages enabled, and German is also the
site's default language, still when users have English as their default
language, they will receive an English e-mail.
