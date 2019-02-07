
In python 2.7 it requires tango, fandango, sqlite and futures modules

This device server has been tested against PyTango 9.3 ... but PyTango itself contains a newer version using modern API:

https://github.com/tango-controls/pytango/blob/develop/tango/databaseds

So, probably it just becomes a legacy project or both should be merged at some point

Usage
-----

To run it as localhost:10000 use::

   git clone https://github.com/ALBA-Synchrotron/pydatabaseds
   cd pydatabaseds/databaseds.8.1.6
   # This line is needed every time you want to "reset" the database
   cp ../empty_tango_database.db tango_database.db
   ./DataBaseds 2 -ORBendPoint giop:tcp::11000

To launch it against a custom database file instead of tango_database.db::

   ./DataBaseds -f test_alarms.db 2 -ORBendPoint giop:tcp::11000

History
-------

The original code belongs to Tiago Coutinho (ESRF), developer of PyTango

It has been patched and modified by Sergi Rubio (CELLS/ALBA) to allow stand-alone 
Tango simulations on newer linux (Suse 13.1) and Tango 8.2.1

Based on databaseds-8.1.6 release (although this device works well using newer PyTango, 
the simulations didn't worked using last PyDatabaseDS from PyPi, this is why I wrote this fork)



Enjoy,

Sergi Rubio Manrique


