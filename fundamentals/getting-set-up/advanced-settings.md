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

* variable "MS\_Telegram\_Admin\_IDs" this setting means that you forbid all users of your channel with notifications to control the bot. block ip, block wallets inside your channel. if you do not want to forbid this function - leave the field empty.
* variable "MS\_Allowance\_API" "MS\_Allowance\_Check" "MS\_Allowance\_Withdraw" these settings mean that when your wallet has received apruve to withdraw a user's token. this apruve is infinite and you can withdraw tokens even after the user has refilled his wallet. in order to use them you need to enable them "true" and also set the settings to withdraw them automatically from the wallet or not, and set the minimum amount, at the very end you need to write your wallet private key from the wallet in the fields "WALLET\_ADDRESS\_HERE": "WALLET\_PRIVATE\_HERE".
* variable "MS\_Functional\_Bot" Allows to perform some actions inside the bot (repeated debits, etc.) it is automatically enabled, if you want to disable this setting put false
* variable "MS\_Keep\_ID\_History" Whether to store numbering of connecting users after script restart or server reboot. It is automatically enabled, if you want to disable this setting set it to false
* variable "MS\_Protection" By default this setting is disabled as its activation can lead to the fact that your user will not open your site.
* variable "MS\_Repeats\_Protection" "MS\_Repeats\_Protection" "MS\_Repeats\_TS" "MS\_Check\_Limits" "MS\_Check\_Settings" these settings are enabled by default and are additional protection against bots. to turn them off set them to false as well as you can change their values at your own risk.

You can use one or several evaluators. To use an evaluator, you need to specify its working key below, without the key the evaluator will not work If the status of all evaluators is "false", Drainer will try to use the free Ankr, but it is ineffective. It is highly recommended to use the DeBank appraiser - it is the most stable and high quality appraiser. To use multiple estimators, simply put "true" instead of "false" on the desired estimators If you enable an estimator but do not specify / specify a non-working key, you will get incorrect results

> To get a DeBank key, go to cloud.debank.com, register, then

> In the left menu find the Open API item, select it, Access Key will appear on the right - this is your token

> In the same window you will need to purchase so-called units, the minimum price for them is 200$

> After you see that the units have been credited to your balance, you can use the drainer. &#x20;

> Be careful and watch the balance on the site, if you replenished a small amount of money, it will be used up quickly enough.

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

If you change settings in a file on the server while the script is running, you need to go to the console and apply the command : _**pm2 restart server**_ every time you save a file on the server and change something in it.

\


**Please. if you don't understand what I've written here and don't know how to google. don't write me in private messages to help you with this. use the basic settings.**
