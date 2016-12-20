## Setup a new Windows Development Environment

Start Microsoft Edge (chrome/firefox do not work) and run:
```
http://boxstarter.org/package/nr/url?https://raw.githubusercontent.com/rjpass/windows-development/boxstarter/boxstarter
```

After this finishes, reboot your machine.

Next, run these commands from an admin PowerShell:
`npm install -g npm-windows-upgrade`
`npm install -g npm@3.5.0`
`npm install -g --production windows-build-tools`

This will not install `docker`, `slack`, or `netbeans`.  It will also not install the unlimited strength policy jars.  You will need to install them manually.

You will also need to update the system PATH to include `%ANT_HOME%\bin`.

In the Docker sys icon tray, right click and go to `Setttings`.  On `Shared Drives`, select "C".  on `Advanced`, change CPU to 6 and Memory to 16GB.

## NPM

I would move your default node_modules to somewhere other than Program Files: http://stackoverflow.com/questions/19874582/change-default-global-installation-directory-for-node-js-modules-in-windows

  in C:\Users\{username}\, create .npmrc file with contents:  `prefix = "C:\\Users\\{username}\\AppData\\Roaming\\npm"`

## Optionals:

`choco install tortoisegit`


## Git credentials

Git will work with Git Credential Manager.  This uses Window's credential manager to securely save your passwords for github.  You will however need to clone using http for this to work.

IE: `git clone https://github.com/CleoDev/EFSS.git`  

If for whatever reason you have multiple git usernames you would like to maintain, you can issue `git config --global credential.usehttppath true` to seperate creds based on different repositories.
