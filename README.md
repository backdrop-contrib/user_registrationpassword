User Registration Password
==========================

This module allows people to set a password during registration when the setting
for 'Email verification & password' is set to: 'Require a verification e-mail.
Allow people to set a password on the registration form.'.

By default, users can create accounts directly on the registration form, set
their password and be immediately logged in, or they can create their account,
wait for a verification e-mail, and then create their password.

With this module, users are able to create their account along with their
password and simply activate their account when receiving the verification
e-mail by clicking on the activation link provided via this e-mail.

User Registration Password transforms the "Require email verification when a
visitor creates an account." checkbox on the Account settings page into a list
of 3 radio options.

The first 2 are default Drupal behaviour:
0 Do not require a verification e-mail. Allow people to set a password on the
  registration form.
0 Require a verification e-mail. Account must be verified before a password may
  be set.

The newly added option is:
X Require a verification e-mail. Allow people to set a password on the
  registration form.

The first 2 disable User Registration Password, only the 3rd option activates
the behaviour offered by this module.

Installation
------------

- Install this module using the official Backdrop CMS instructions at
  https://backdropcms.org/guide/modules

- Visit the Account settings configuration page under Administration >
  Configuration > User accounts > Account settings
  (admin/config/people/settings) and review the setting for 'Require email
  verification when a visitor creates an account'.

- Visit the Account email configuration page under Administration >
  Configuration > User accounts > Emails (admin/config/people/emails) and
  update the welcome email message text, as necessary.

Documentation
-------------

Additional documentation is located in the Wiki:
https://github.com/backdrop-contrib/user_registrationpassword/wiki/Documentation

Issues
------

Bugs and Feature requests should be reported in the Issue Queue:
https://github.com/backdrop-contrib/user_registrationpassword/issues

Current Maintainers
-------------------

- Jen Lampton (https://github.com/jenlampton)
- Seeking additional maintainers

Credits
-------

- Ported to Backdrop CMS by [Jen Lampton](https://github.com/jenlampton)
- Maintaiend for Drupal by [Rob C](https://www.drupal.org/u/rob-c).
- Originally written for Drupal by [jide](https://www.drupal.org/u/jide).

License
-------

This project is GPL v2 software. See the LICENSE.txt file in this directory for
complete text.


