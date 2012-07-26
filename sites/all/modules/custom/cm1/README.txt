/**
 * CURRENT
 */
Instructions:
- Overwrite the old version of cm1 module with the new version
- Clear all caches
- Go to "admin/structure/cm1", select the mailchimp list name and save.

There are four new files inside cm1 folder as follows:
- cm1-initialstate.tpl.php
- cm1-invalidemail.tpl.php
- cm1-alreadysignedup.tpl.php
- cm1-success.tpl.php

In order to alter the look of any state, you should copy these files inside your theme folder and enter your html and your styles accordingly.

/**
 * OUTDATED
 */
Instructions:
- upload this module to your site
- enable it (it is called "Custom Module 1")
- go to "/admin/structure/cm1" to configure the screens.
- path alias "subscribe" will be used by this module.

The module implements a settings page to configure the layout of the
mailchimp form. The settings page can be accessed at
"/admin/structure/cm1". There you will find sample html for the "Stay
Informed" link. Also, two text areas to configure the layout of the
subscribe screens.

When you click on "Stay Informed" link, a colorbox will open with the
contents of "Screen 1". You should see a list of tokens below the
"Screen 1" text area. Each token will render a Mailchimp form. You
should use only the one that you need. You can enter HTML above and
below the token.

The second text area is for entering the HTML that will appear inside
the colorbox after the form has been successfully submitted. You can
enter HTML as well.