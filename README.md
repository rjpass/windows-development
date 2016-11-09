## Setup a new Windows Development Environment

Start Microsoft Edge (chrome/firefox do not work) and run:
```
http://boxstarter.org/package/nr/url?https://raw.githubusercontent.com/rjpass/windows-development/boxstarter/boxstarter
```

After this finishes, reboot your machine.

This will not install `docker` or `netbeans`.  It will also not install the unlimited strength policy jars.  You will need to install them manually.

You will also need to update the system PATH to include `%ANT_HOME%\bin`.

Git will work with Windows Credential Manager.  This uses Window's credential manager to securely save your passwords for github.  You will however need to clone using http for this to work.

IE: `git clone https://github.com/CleoDev/EFSS.git`  

If for whatever reason you have multiple git usernames you would like to maintain, you can issue `git config --global credential.usehttppath true` to seperate creds based on different repositories.
