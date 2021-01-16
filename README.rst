Limit Phone Number Country
==========================

This is a plugin for `pretix`_. 

Limit the available phone number country code in pretix phone number questions. Caution! Applies to the whole server!
This plugin does not even have to be activated. As soon as you install it, it overrides the phone number prefixes
available server-wide.

It applies to both phone number questions and the pretix built-in phone number field.

By default, this plugin restricts phone numbers to "+1 (USA)". If you want to
place a different restriction, you can do so via the pretix configuration file.
Add a section like this (and use the standard country codes)::

   [plugin:limit_phone_country]
   US = 1
   DE = 49

Development setup
-----------------

1. Make sure that you have a working `pretix development setup`_.

2. Clone this repository, eg to ``local/pretix-limit-phone-country``.

3. Activate the virtual environment you use for pretix development.

4. Execute ``python setup.py develop`` within this directory to register this application with pretix's plugin registry.

5. Execute ``make`` within this directory to compile translations.

6. Restart your local pretix server. You can now use the plugin from this repository for your events by enabling it in
   the 'plugins' tab in the settings.


License
-------


Copyright 2021 Tobias Kunze

Released under the terms of the Apache License 2.0



.. _pretix: https://github.com/pretix/pretix
.. _pretix development setup: https://docs.pretix.eu/en/latest/development/setup.html
