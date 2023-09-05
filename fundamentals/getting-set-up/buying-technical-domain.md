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

# 4⃣ Buying technical domain

Before buying domains, we need to register an account on the cloudflare platform.

Go to [https://www.cloudflare.com/](https://www.cloudflare.com/) and register.

After that we need to register 1 domain:

* **Technical domain** - it can have any name and zone. it is needed only for the correct operation of the drainer. This domain will not be seen by visitors to your site.

For these purposes, I will use the registrar [https://www.namesilo.com/](https://www.namesilo.com/)

Register on this site, top up your balance and buy your first domain

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

Now I have registered a **technical domain**, the drainer script will work on this domain. You need to set it up correctly. To do this, copy the domain name and go to the site [https://dash.cloudflare.com/](https://dash.cloudflare.com/)

Click on the "Add a site" button

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Enter the name of the **technical domain** and click "continue"

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

Choose a free plan and click "Continue"

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

In the window that appears, we need to copy the values of **Nameserver 1** and **Nameserver 2**

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

Go to the site [https://www.namesilo.com/account\_domains.php](https://www.namesilo.com/account\_domains.php) \
Select the **Technical domain** and from the top menu select "Change Nameservers"

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

In the window that appears, insert the new Nameserver 1 and Nameserver 2, which we received on the Cloudflare service and click "submit"

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

After the changes are saved, go to the website [https://dash.cloudflare.com/](https://dash.cloudflare.com/) To the section "SSL/TLS - Overview". Change the parameter to "**Flexible**"

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

Then go to the "SSL/TLS - Edge Certificates" section. The "Always Use HTTPS" feature must be enabled.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

Go to the "DNS - Records" section and click "Add Record"

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

We create a new record. In the "Type" field, select "A" In the field "Name" write "@" In the "IPv4 address" field, write the IP address of the server that we bought on the [https://cp.zomro.com/services/vps](https://cp.zomro.com/services/vps) website and click save.

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Please note that changing server names can take up to 24 hours. Usually changes occur much faster, up to 1-2 hours. Now if we navigate to our **technical domain** address "https://goldendrainer.top/" we should see the response "Sorry, this page in unavailable". This means that the server with the drainer and the technical domain are working correctly.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption><p>This answer means that everything is correct</p></figcaption></figure>

