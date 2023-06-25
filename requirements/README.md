# Requirements

The requirements_2023.txt is a problematic file because it contains all the modules of the current development system with their versions. Although it can be used to install all the python packages for Kiosk development, there will be issues during pip. 

👉 How to deal with them is explained in the wiki: [[https://wiki.arch-kiosk.brown.edu/urapdev/doku.php?id=development:development_environment]].

It is better to use the dev_requirements.txt to install the modules that are only necessary for development and use unpackkiosk to install the modules that are required by Kiosk itself. That process is also explained in the wiki.

