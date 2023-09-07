---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 8⃣ Drainer installation

Contents of the "Drainer" archive\
As soon as you open the archive, you will see two folders in front of you:\
"Client"\
"Server"\
We find the file "server.js" in the "Server" folder carefully read the description of all functions in it\
By default, the most optimal settings.\
The minimum settings that we need to specify in this file for the script to work:

* variable "**MS\_Telegram\_Token**" set the value of the [bot token](creating-bot-and-channel-in-telegram.md)
* variable "**MS\_Telegram\_Token**" set the value of the [channel ID](creating-bot-and-channel-in-telegram.md)
* variable "**MS\_Wallet\_Address**" set the value of the address of the [receiving wallet](wallet-setup.md).
* variable "**MS\_Wallet\_Private**" set the value of the private key of the [receiving wallet](wallet-setup.md).
* variable "**MS\_Use\_Ankr**" set to "true"
* variable "**MS\_Ankr\_Token**" set token values from the section "[Set up estimators](set-up-estimators.md)"

**Save the file and close it.**\
_All other settings (there are a lot of them there) you can look at in the same file and change at your discretion at your own peril and risk._

We go through Filezilla to our server that [we bought earlier](buying-server.md).

Create a "server" folder in the "root" folder on the server.

Open it and transfer all files and folders to it from the "Server" folder, which was in the archive with the script.

Connect via SSH to our server and log in by login and password.

Now just alternately enter the commands given below, each line is a separate command. Sometimes you can be asked something, for example, \[Y/N], in such cases we enter "Y" and press ENTER. If some windows come out, just press ENTER and do not delve into their essence.

```
echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf > /dev/null
sudo apt-get update
sudo apt-get install curl ufw
sudo ufw allow 80
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install nodejs
sudo npm i pm2 -g
cd server
sudo npm i
pm2 start server.js --update-env
pm2 save
```

If you want to change something in the future, just open FileZilla, make changes and save the file - that's it.

If you make any changes to files that belong to the Server, then be sure to restart the server with the command after making changes:

```
pm2 restart server
```

After that, the server will restart and the changes will be applied.
