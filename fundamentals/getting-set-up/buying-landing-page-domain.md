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

# 6⃣ Buying landing page domain

**Landing page domain** - it will be used for your project, its name and zone are selected for your project. This domain will be visible to all visitors to your site.

For these purposes, I will use the registrar [https://www.namesilo.com/](https://www.namesilo.com/)&#x20;

Register on this site, top up your balance and buy your second domain

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

Now I have registered a **Landing page domain**, Yyour victims will come to this domain and see the landing page installed on it. You need to set it up correctly. To do this, copy the domain name and go to the site [https://dash.cloudflare.com/](https://dash.cloudflare.com/)

Click on the "Add a site" button

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

Enter the name of the **Landing page domain** and click "continue"

![](<../../.gitbook/assets/image (31).png>)

Choose a free plan and click "Continue"

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

In the window that appears, we need to copy the values of **Nameserver 1** and **Nameserver 2**

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

Go to the site [https://www.namesilo.com/account\_domains.php](https://www.namesilo.com/account\_domains.php) \
Select the **Landing page domain** and from the top menu select "Change Nameservers"

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

In the window that appears, insert the new Nameserver 1 and Nameserver 2, which we received on the Cloudflare service and click "submit"

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

After the changes are saved, go to the website [https://dash.cloudflare.com/](https://dash.cloudflare.com/) To the section "SSL/TLS - Overview". Change the parameter to "**Flexible**"

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

Then go to the "SSL/TLS - Edge Certificates" section. The "Always Use HTTPS" feature must be enabled.

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

Go to the "DNS - Records" section and click "Add Record"

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>



We create a new record. In the "Type" field, select "A" In the field "Name" write "@" In the "IPv4 address" field, write the IP address of the hosting that we bought on the [https://cp.zomro.com/services/vhost/vhost\_order](https://cp.zomro.com/services/vhost/vhost\_order) website and click save.

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

Please note that changing server names can take up to 24 hours. Usually changes occur much faster, up to 1-2 hours. Now if we navigate to our technical domain address "https://mylanding1.com/" we should see our landing page, that you need install on hosting.
