![Image 1](/img/portal.png)

![Image 2](/img/estadoaps2.png)

![Image 3](/img/parajin2.png)

![Image 4](/img/membersadmin.png)

![Image 5](/img/owncloudrsc.png)

![Image 6](/img/croquis.png)

![Image 7](/img/rexistro7.png)

![Image 8](/img/estadisticaspersoais.png)

![Image 9](/img/webmail.png)


### This is my cornerstone

* * *

Firstable, had to say that **ALL the programming and server-based work showed here are FULLY designed and developed by me.**

**RianxoSenCabos** was a non-profit technology and wireless networking association that consisted of a metropolitan area network **(MAN) of +100km2**, wich I've mainly manage and develop over the years, based in 3.4Ghz and 5Ghz wifi access points. Initialy was just a network to give internet connection to rural areas without a public infrastructure, and to share contents and knoledge between the members (clients), but it becomes in something just way bigger at the time **I fully developed** from a captive portal to a bunch of services in a central server, just as:

*   **Own social network**, based in a [Diaspora Pod](https://diasporafoundation.org/)
*   **Email server and webclient** with Postfix, Sendmail, Dovecot, Spamassassin, Roundcube
*   **Personal cloud** storage with
*   **Utorrent Server** and own developed **webportal** to search and download items in our own site
*   **Streaming server** with [Subsonic](https://www.subsonic.org/), to stream andy downloaded content, besides of each client private Owncloud storage files
*   **Client-side administration portal**, to see transfer stats, access data, signal of your wifi conection, and PayPal integrated payments (the associacion had a subscription fee of 16€/month)
*   **Admin-Side administration portal**, where we can see transfer details of clients, devices conected (by mac), signals, and where we can banned, send warnings, etc...

All of this working with:

*   Customized [OpenWRT](https://openwrt.org/) distro at the wireless end-points and [Coova](https://coova.github.io/) captive portal
*   Against a **RADIUS server** backed with [FreeRADIUS](https://freeradius.org/) in a MySQL database
*   Registration by invite or **PayPal automatic payment system**
*   All hosted in an own [Debian](https://www.debian.org/) server with **RAID 10 storage system**, with 3 LANS (internal network and 2 different internet connections)
*   Secondary server **(emergency server)** in another location included in the network as well as with a third internet conection

![First slide](/img/estadisticaspersoais.png)![Third slide](/img/estadoaps2.png)![Second slide](/img/membersadmin.png)![Third slide](/img/datoscliente3.png)

PreviousNext

### Admin and management system

* * *

Our **admin panel** consisted in a series of scripting that **unified the wireless session of each member on our access points (AP's) with a mysql database** where we share data among all our services (from social network to utorrent gui). In addition, **our server scrapped AP stats** (from live clients power&noise to devices connected, macs...) and checked they status every minute, to control members bandwitch use and online time of each one. In the admin panel, **members could see her live SNR, bandwitch, they devices history, user data and password, accounting status...**. I even developed a payment gate through paypal so they can just set a monthly automatic payment or pay when they want. The server banned each slow payer member after 15 days of delay.

We, as admins, had a little different panel where to see the info of all clients in one page, and where we were able to **ban, renew, and manage every member**, besides been able to get any information of they sessions, devices, bandwitch... etc We also had a page to see last 24h of the AP's online status history in a graphical way.

The scripting beyond all of that was made in PHP and helped with some UNIX bash scripts in cron tasks.

### RsC Portal

* * *

All members had an account on **RsC Portal**, where the captive portal redirects them after a successful login. It had a **main page with an embedded search engine** (by google) and an few customizable **quick access links** (fully implemented by myself in PHP), and a **pod of the Diaspora project (social-network)**, a kind of, let's say, a facebook but internal only with the members. There we could **entabling a conversation or post news, articles...** or whatever. I **developed also all the scripting to unify the different login services** (Diaspora, the Radius Server, the Web Portal, Owncloud, Subsonic, Utorrent, Webmail...), you just had to register as a member from our website to access all services with one **unique session**. All this in **PHP, using JavaScript calls from the Login page to each service** and getting the cookies of the sessions in the background, at the same time a new session was generated in the access point and the portal.

### Personal email

* * *

With an **own mail system** at the main server, (iRedmail/Postfix/Sendmail/Dovecot/SpamAssassin) we provided all our members with a **hisusername@rianxosencabos.com** email address, and through the portal they could access vía web (Roundcube) to they messages, as well as they could use their personal computer clients through IMAP or POP3.

![First slide](/img/owncloudrsc.png)![Third slide](/img/owncloud.png)![Second slide](/img/subsonic.png)![Third slide](/img/utorrent.png)![Third slide](/img/downloader.png)

PreviousNext

### Cloud storage

* * *

We provided **+50Gb of cloud storage** to each member in our OnwCloud (a Dropbox/GDrive/OneDrive open-source webapp). We had a few folders accessible to all members where they share anything they wanted to.

Our Owncloud was also **customized by me, adding an streaming web system (subsonic)** where the members could see any multimedia content hosted on his Cloud accounts or in the shared folders. We also provided an uTorrent server with the correspondent webclient, where members could download any p2p content directly to the shared folders.
