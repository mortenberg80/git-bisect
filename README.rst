git bisect
==========

This project demonstrates how git bisect works.

Manually
--------
You can demonstrate this by the following commands:
* git bisect start
* git bisect bad master
* git bisect good b6911ee
b6911ee points to my initial commit
Then use:
* git bisect <good/bad>
until you find your commit

Automatically
-------------
* git bisect start master b6911ee
* git bisect run mvn clean install

The first command is a shorthand command for commands 1-3 in the "manually"-instructions.
The second command starts the bisect process, and runs the given script to check if the commit is good or bad. In this example I use Maven, but you could also use other scripts, as long as they return the proper exit codes.
