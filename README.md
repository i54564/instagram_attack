# Instagram dictionary attack

**NOTE:** For educational puposes only, I do not take credit for any harm, that has been done with this software.

This is a dictionary attack for instagram, using Python.

![Insta prev](images/insta.png)


***You will need to install some modules for the scripts to run:***

 ```pip install selenium ```
 
 ```pip install stem  ```
 
 ```pip install optparse-pretty```
 
 ```pip install beautifulsoup4```
 
 **Keep it in mind, that you have to have TOR configured for this.**
 
 **You have to have port 9050 and 9051 opened and used by TOR**
 
 
 For port 9051 to work, you have to change the **torrc** file.
 
 Find this part in the file:
 ```
 ## The port on which Tor will listen for local connections from Tor
## controller applications, as documented in control-spec.txt.
# ControlPort 9051
## If you enable the controlport, be sure to enable one of these
## authentication methods, to prevent attackers from accessing it.
# HashedControlPassword (Your hashed password will be here)
# CookieAuthentication 1
 ```
 
 **NOW uncomment the following (remove the # sign)**
 
 ```
 # ControlPort 9051
# CookieAuthentication 1
 ```
 
 **SAVE the file**, and start up TOR.
 
 ```tor.exe -f torrc```
 
 **NOTE**  Any passwords that are less than 6 characters, are getting an extra "1111", to their end, as Instagram, would not let me to press the login button. Also you cannot have a password, that is less than 6 characters....
 
 ***USAGE of the script***
 
 ``` 
 Usage: insta.py [-u] username [-l] passwordlist

    REQUIRED:
        -u or --username: The username of the victim
        -l or --list: The password list to be used 
    HELP:
        -h or --help
```
