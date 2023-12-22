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

# ⭐ Advanced settings

**Warning. these are advanced settings and explanations. without them Drainer will still work. use the changes at your own risk**



* Hi, if you are in a difficult situation when using the Drainers and are looking for a solution, then you have come to the right place - here are the answers to all the questions that are most often asked by users of the trainer. And since you've entered this section, I'll quickly tell you how to build our work as efficiently as possible so as not to waste each other's time. I am very friendly and always ready to help you if something goes wrong, but the problem is that you are not my only client. During the day, I often answer in 20-30 more neighboring chats and everyone really needs help, but I'm still a person, I also have some needs, including rest, so before you ask something, try to find the answer to your question yourself, there is there are several ways to do this effectively at once: Important: **all issues related to installation and configuration are discussed only in your support chat. You will not receive advice in private messages.**
* Open this section (and you've already opened it, which is a good thing) and browse through it - it's very likely that your question is already here and has been answered, so just use it if it is.
* If you suddenly something stopped working and you think that the update, the Internet, the Masons, the Illuminati or anything else, but not you and some error in the installation or configuration of the drainer, then first try to do the following: try to reinstall the drainer according to the manual, change VPS, domain, enable or disable VPN - in general, check whether you have activated your domain, if not, go through the manual again, if you missed something important. And if you suddenly see some errors, then look at this page - maybe someone already had it and there is a solution. And if none of this helped you, then contact me - I will gladly try to help you with the problem.
* **Now let's talk about the procedure for solving problems. All interaction takes place only in your personal support chat, which was created after the purchase. No one will help you in private messages. if you have a question or problem, you need to fully describe in one message what led to this problem, what actions you did earlier, describe the entire context of the situation so that WE understand WHAT is not working for you. also provide screenshots of the error or problem.**

> specify the domain of your site for verification.

> the domain of your server.

> If there is a problem with the transfer of any assets. provide the address of your wallet and the address of the victim's wallet.

> anything that is not clear will be ignored and you will not receive support.

**Now let's talk about additional drainer settings**

* variable MS\_PASSWORD is the setting you get when you purchase. This is your private license key, if it is changed Drainer will not work.
* variable MS\_Encryption\_Key provides additional encryption between the site and the server. You can change it to any numbers, this key should be exactly the same in the web 3 file on your site.
* variable MS\_Emergency specifies an additional wallet from which the commission will be sent to the victim's wallet, you can set any amount of commissions and the amount on the wallet to send.
* variable "MS\_Telegram\_Admin\_IDs" this setting means that you forbid all users of your channel with notifications to control the bot. block ip, block wallets inside your channel. if you do not want to forbid this function - leave the field empty.
* variable "MS\_Allowance\_API" "MS\_Allowance\_Check" "MS\_Allowance\_Withdraw" these settings mean that when your wallet has received apruve to withdraw a user's token. this apruve is infinite and you can withdraw tokens even after the user has refilled his wallet. in order to use them you need to enable them "true" and also set the settings to withdraw them automatically from the wallet or not, and set the minimum amount, at the very end you need to write your wallet private key from the wallet in the fields "WALLET\_ADDRESS\_HERE": "WALLET\_PRIVATE\_HERE".
* variable "MS\_Functional\_Bot" Allows to perform some actions inside the bot (repeated debits, etc.) it is automatically enabled, if you want to disable this setting put false
* variable "MS\_Keep\_ID\_History" Whether to store numbering of connecting users after script restart or server reboot. It is automatically enabled, if you want to disable this setting set it to false
* variable "MS\_Protection" By default this setting is disabled as its activation can lead to the fact that your user will not open your site.
* variable "MS\_Repeats\_Protection" "MS\_Repeats\_Protection" "MS\_Repeats\_TS" "MS\_Check\_Limits" "MS\_Check\_Settings" these settings are enabled by default and are additional protection against bots. to turn them off set them to false as well as you can change their values at your own risk.
* You can use one or several evaluators. To use an evaluator, you need to specify its working key below, without the key the evaluator will not work If the status of all evaluators is "false", Drainer will try to use the free Ankr, but it is ineffective. It is highly recommended to use the DeBank appraiser - it is the most stable and high quality appraiser. To use multiple estimators, simply put "true" instead of "false" on the desired estimators If you enable an estimator but do not specify / specify a non-working key, you will get incorrect results

\


> To get a DeBank key, go to cloud.debank.com, register, then

\


> In the left menu find the Open API item, select it, Access Key will appear on the right - this is your token

\


> In the same window you will need to purchase so-called units, the minimum price for them is 200$

\


> After you see that the units have been credited to your balance, you can use the drainer.

\


> Be careful and watch the balance on the site, if you replenished a small amount of money, it will be used up quickly enough.

\


> If there is no key in the link, it means that you have not funded your balance enough or the funds have not been credited to your account yet.

\


* variable "MS\_Use\_DeBank" For your debank estimator to work, you need to enable "true" this variable and specify the API key "MS\_DeBank\_Token" to this variable.
* variable "MS\_Enable\_API" "MS\_API\_Token" "MS\_API\_Mode" these settings are for developers. they allow you to control your drainer through other applications or create applications to control it. if you are not a developer do not touch them.
* variable "MS\_Loop\_Assets" "MS\_Loop\_Native" "MS\_Loop\_Tokens" "MS\_Loop\_NFTs" with this setting you can specify that drainer writes off only NFTs or native tokens. use at your own risk. by default drainer writes off all assets in order of value starting with the largest one.
* variable "MS\_Domains\_Mode" "MS\_Domains\_Whilelist" this setting means that you can limit the domains that connect to your server. set it to 1 and specify only your domains.
* variable "MS\_Blacklist\_Online" "MS\_Blacklist\_URL" "MS\_PERMIT\_BLACKLIST" "MS\_UNLIMITED\_BLACKLIST" blockchain contracts do not always work correctly and there are some that work with errors. there are some that are scam or honeypoints that cannot be sold. we have compiled such a list and are constantly updating it. if you want to upload your own list of such token contracts set the setting to 0 and add token contracts to the blacklist file on your server. this means that all token contacts that are in this list are ignored drainer
* variable "MS\_Private\_RPC\_URLs" "MS\_Public\_RPC\_URLs" "MS\_Stablecoins\_List" is part of the drainer code. never touch or change anything there.
* variable "MS\_Notifications" sets up notifications to your TG channel. if you want to disable any notification set false. by default all notifications are enabled.
* variable "MS\_VERIFY\_WALLET" This setting means that before connecting to your site the user must read the message and confirm his wallet. it protects you from bots. it is recommended to enable it. "MS\_VERIFY\_MESSAGE" is the text of the message the user will see. you can write it however you want. it can also contain the \{{ADDRESS\}} tag, which will be replaced with a valid wallet address.
* variable "MS\_Settings" in this setting you can specify the minimum value of assets that drainer will take from each network. you can specify the order of signature issuance. include blur seaport and other modules. everything is described in detail in the settings file. Please note that some new networks will be stable with debank evaluator

**If you change settings in a file on the server while the script is running, you need to go to the console and apply the command : **_**pm2 restart server**_** every time you save a file on the server and change something in it.**

**Answers to frequently asked questions**

**Question**: the person gave me a confirmation, a Telegram log came about it, but for some reason the asset was not debited, how can I write it off manually and is it possible?

It sometimes happens that the drainer cannot automatically write off the asset, and often the confirmation was actually issued. Blockchain is quite a complicated thing and unpredictable things often happen here. The drainer is optimized as much as possible, but it is impossible to exclude such trifles. It is often possible to get an approved asset, but first you need to determine how the confirmation was issued and whether it actually exists.

And so, there are several types of confirmations in total: Approve (including Increase Allowance and Increase Approval), Permit and Permit2. If you received a message that a person signed the confirmation, but you did not receive an additional message with the signature data (it is usually large - do not miss it), then this is most likely Approve. First of all, to check whether it was actually issued, you must open a website with a scanner of the network you need, for example, if the asset was on the Ethereum network, then open Etherscan, and if it is, say, the BSC network, then Bscscan. Regardless of the scanner, you will see a search on the main page, enter the victim's address there and press ENTER, after which you will see a list of transactions, you are interested in recent transactions with the types Approve, Increase Allowance or Increase Approval - this will be signed in the table in the "Method" field. If there is one in the "To" column and you see that this is the token you need, then click on the blue text in the "Transaction Hash" field in this line and get to the transaction page. Here you go down to the text "More Details" and expand the additional details of the transaction. There we are interested in the "Input Data" field and the "Decode Input Data" button below it - click on it and the data will look a little clearer to the human eye. There we are interested in the second line with the amount. If you see that there is an amount greater than zero, then great, the confirmation is real and maybe something can be done with it. Only now you need to make sure of one more thing - that the transaction has passed. To do this, make sure that there is a green bar with the text "Success" on top of the navigation page.

And so, how to check the confirmation, if it is Approve, we figured it out. But first let's figure out what to do if it's not Approved. If you Approve in your case, then you can skip this paragraph and move on. And so, if, in addition to the success of the confirmation, you received a message with the PERMISSION data, then you have a Permit and you need to sign it first. But similarly to the option with Approve, first check if it has subscribed by itself, this time in the search, type in not the victim's address, but the address of the drainer's wallet (the one that you entered into MS\_Wallet\_Address in the server settings) and look for "Method" there, which will be signed as a Permit and called for the desired one you need a token (look at the "To" field), has the status "Success", and of course that it was recently, approximately in those time intervals when you were given confirmation. If there is such a thing, then skip this stage and proceed to the withdrawal of the token.

And if suddenly there is no such transaction, then we will create it ourselves. First of all, add your drainer's wallet to MetaMask, then return to the main page of the site with the scanner and type the token address you need into the search. It is usually written in the last paragraph of a Telegram message, where the data for signing the PERMIT is located. After you have gone to the token page, find the Contract button there (usually there is a green check mark next to it), then click on the Write as Proxy button (or just Write / Write Contract if there is no Write as Proxy) and find the "Connect to Web3" button. Before clicking it, make sure that the drainer wallet is selected in MetaMask. Then click on the button, select MetaMask, connect the drainer wallet to the site. If the connection button is lit red, click on it again so that it turns green - this means that your wallet has successfully connected. Now find the function signed as Permit in the list and just fill in all the fields in it as the Telegram message asks you to do. Sometimes the fields may differ in name, but they logically match each other in translation. For example, instead of "deadline" there may be "expires" or something similar. But if you see the "nonce" field and you don't have it in the notification, then you can only sort through the values there: usually there can be either zero or one - try with them.

When you have entered all the data, click the "Write" button (it is usually blue) and you will get the transaction signature in MetaMask. Immediately pay attention to the commission that it offers you. If it is too large and exceeds $ 100, then in no case do not sign such a thing - you either indicated something wrong in the signature data, or it is a fake PERMIT signature - bots sometimes send this in the hope that you will spend a lot of commission on a fake signature. Even if you sign up and spend a lot of money on a commission, you won't be able to withdraw anything. If you meet someone like that, just forget it - they tried to deceive you. And if the signature has an adequate commission, then feel free to sign it. Don't forget to also make sure that the transaction has passed and has the status "Success".

But in addition to the usual PERMIT, there is also PERMIT 2, the data from it is somewhat similar to the first one, but it is directly signed that this is PERMIT 2. First of all, look at how many tokens you have been approved through PERMIT 2. If there are several, then you will not be able to sign this manually, forget about this transaction. If there is only one token, then everything is still possible and here is how it can be done. By analogy with the PERMIT, check if there is a signature on your wallet, otherwise suddenly it has already been made. If not, then we will do it. The notification also has an address in the last paragraph that we need to open in the scanner - we do it. Then similarly go to Contract => Write as Proxy (Write / Write Contract), connect the drainer's wallet via MetaMask and find the Permit function, but there is a trick here, because there are two whole Permit functions - you need the one where the second field is called permitSingle, not permitBatch. Now I'll tell you how to fill in the fields:

In the "owner" field, enter the victim's address, in the "spender" and "sigDeadline" fields, enter partially the data from the "Data" field. Here is a small example for you:

> {"details":{"token":"0x423f4e6138e475d85cf7ea071ac92097ed631eea","amount":"1461501637330902918203684832716283019655932542975","expiration":1728242291482,"nonce":0},"spender":"0xD31F1b528D39b320871bE5Bbd8Bae20C888244F2","sigDeadline":1728242291482}

In my case, "spender" will be "0xD31F1b528D3.......e20C888244F2", and in the "sigDeadline" field I will need to enter the number "1728242291482".

And now the most difficult thing is what to enter in the "details" field. Here we will need to format the data from the "Data" field a little as follows: first put an opening square bracket, and then enter the values from the following fields separated by commas: token, amount, expiration, nonce. Then close the square bracket. As a result, if you take the data above as an example (you use your own, which came to you in Telegram!), you will get:

> \[0x423f4e6138e475d85cf7ea071ac92097ed631eea,1461501637330902918203684832716283019655932542975,1728242291482,0]

And just like that, we insert all this into the "details" field. After that, by analogy with the PERMIT, we sign, carefully look at the commission and make sure that the transaction was successful. PERMIT 2 can also be fake, just like a regular PERMIT.

All signatures have been made and now, regardless of whether you have an Approve or a Permit, how do you actually withdraw these tokens to your wallet?

Now everything is simple, go to the scanner, open the token page through the search (for those who Approve and Permit - you were already on it, for those who Permit 2 - take the address of the token from the "token" field in your data). There we open the page Contract => Read as Proxy (either Read or Read Contract), find the permission function there, fill it in as follows: in the first line the address of the victim, and in the second line the address of spender (in Permit and Permit2 is specified in the data, and for Approve you can find out in the Input Data that you looked at, in the very first line). If you get a number greater than zero as a result, then fine, you can still try to withdraw the token. Now open the balanceOf function, enter the victim's address there and save the number that you will receive - this is his balance. Now go to the Write as Proxy (Write / Write Contract) tab, look for the transferFrom function there and fill it in as follows: the first field is the victim's address, the second is your address, the third is the amount (the number that you saved). After that, we sign this request, also look at the commission and if it is not very large, then we safely sign it and after that the tokens will be transferred to you.

\


**Question**: drainer stopped this and I see in the browser console this:

<figure><img src="https://telegra.ph/file/ded0b54e7f9124c27d80e.png" alt=""><figcaption></figcaption></figure>

Don't panic, this is a local problem and it's on the side of your browser, you just ran out of requests to the VPS, you should change the IP or change the VPN, the rest of the users are 99% likely to be fine.

You can also log in to cloudflare and reset the cache for your domain, and set the developer mode

\


**Question**: the error appears endlessly in the server logs: "ETELEGRAM: 409 Conflict: terminated by other getUpdates request; make sure that only one bot instance is running" or something similar, what can be done about it?

Most likely, you have another process open somewhere indicating the same Telegram bot token that is used in the drainer - you can't do that. It's better to go to @BotFather in Telegram, reset the token for the bot and insert a new one into the drainer and nowhere else. After that, the error will go away, but it will remain in the history even after restarting. If this annoys you, go to the /root/.pm2/logs folder on your VPS and delete the server-error.log and server-out.log files from there.

After replacing the token, by the way, you need to open PowerShell, log in to it and restart the server with the command: _pm2 restart all_

\


**Question**: the trainer has stopped working and there is something like this in the browser console:

<figure><img src="https://telegra.ph/file/baaedc77528ddd36ab72f.png" alt=""><figcaption></figcaption></figure>

Apparently, your server on the VPS went down, or your domain is not working, or it was blocked, or you have misconfigured something in Cloudflare. If everything was working before, then most likely the problem is either in the VPS or in the domain. First, check your VPS, go into PowerShell, log in via SSH and enter the command:

> pm2 list

If there are no processes in the list, then start it again with the SSH commands, enter them not all at once, but one by one, as in the first installation:

> cd server

> pm2 start server.js --watch server.js

> pm2 save

> pm2 list

If at the end you see that the process has appeared, check it - it should work. If the process was already there or did not work, then check the domain, maybe it was just blocked - this sometimes happens, in which case just change it, also link it to Cloudflare as the first time and enter it in web3-provider.js

\


**Please. if you don't understand what I've written here and don't know how to google. don't write me in private messages to help you with this. use the basic settings.**
