ESWL Updater
=================

ESWL is a whitelist maintained by the members of the 
[ABUSES community](http://www.abuses.es/eswl/). This utility is a simple
script + cron file to periodically update the whole whitelist as two
files of CIDR blocks that postfix can understand and check against.

Postfix configuration is left as an exercise for the user.

Installation
------------

Installation is pretty simple. You just have to copy the following
files to their corresponding locations:
  * `etc/default/eswl-updater` -> `/etc/default/eswl-updater`:
    This is the main configuration file, where you can change the route
    to the different utilities and/or postfix configuration files.
  * `etc/cron.d/eswl-updater` -> `/etc/cron.d/eswl-updater`:
    Cron definition file that will execute the utility once a day
  * `bin/eswl-updater` -> `/usr/local/bin/eswl-updater`:
    Main program logic, that updates the files and postmaps them.

It is recommended to check that the default configuration values are
correct for your system.
