Login Register
=============

Creating a login system with registration upon registering an activation link will be emailed containing a link to activate the account. Once active the user can login, a reset option is available to reset the password.

In the classes folder their are two files: password.php and user.php. password.php is used to provide the same hashing capability that exists within php 5.5 it uses the same function names so versions 5.3 - 5.5 can use the same functions.<

Note on password for php versions less than 5.5
This library requires PHP >= 5.3.7 OR a version that has the $2y fix backported into it (such as RedHat provides). Note that Debian's 5.3.3 version is NOT supported.

user.php is a class that contains methods to return the users hash (hashed password) as well as logging in, checking if a logged in session already exists and logging the user out.


Config.php
Config.php will be included into all pages enable sessions and turn on output buffering this way headers can be used anywhere in the project.

Set the timezone and define the credentials for the database, next attempt to make a new PDO connection if the connection fails display the error and kill the page.

Next include the user class and make an instance of it, pass in the database object to the class to make use of the database.

Also ensure your php version is at least 5.3.17 but ideally should be 5.6 or 7
These files acompany the tutorial: [Login and Registration system with PHP](https://daveismyname.blog/login-and-registration-system-with-php)
