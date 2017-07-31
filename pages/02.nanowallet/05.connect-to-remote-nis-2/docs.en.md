---
title: 'Connect to Remote NIS 2'
taxonomy:
    category:
        - docs
---

If you run a NEM node (NIS) with either your [home computer](http://blog.nem.io/easy-configuration-guide-opening-port-7890/) or a free [Amazon t2.micro Linux VPS](http://blog.nem.io/create-a-linux-vps/) or a free [Amazon t2.micro Windows VPS](http://blog.nem.io/create-a-windows-vps/), you can connect to it remotely from anywhere as long as you know the IP address.   
 
If you don't want to run your own server, take a look at the list of public NEM node IPs [here](http://www.nodeexplorer.com/) (this website is not run by the NEM team, so we cannot accept any responsibility for the content).  

**Note:** The [Node Explorer](http://www.nodeexplorer.com/) has an option to sort nodes by country so that you can easily find a node that is close to your location, which results in a faster connection.  
   
The benefits of connecting to a remote server are 1) you can make that server harvest for your account once you have enabled [delegated harvesting](http://blog.nem.io/how-local-and-delegated-harvesting-works/), and 2) you don't have to synchronize the block chain on your local computer to use the NEM wallet, which reduces the preparation time on a new computer to just a few minutes.

####Steps
**1)**	You will need to run NCC. Download [here](http://nem.io/install.html) if you didn't install it yet ([Java 8](http://blog.nem.io/how-to-install-java-8-64-bit-on-windows/) is needed).  
**2)** Once NCC is running, go to the [landing page](http://localhost:8989/ncc/web/index.html) in your browser:

![](/content/images/2015/05/Screenshot-2015-05-31-13-09-24.png)  

**4)**	Click *Settings* in the upper right corner:
![](/content/images/2015/05/Screenshot-2015-05-31-13-11-08.png)

**5)**	In the box labeled *Host*, replace “local host” with the IP address that you have obtained by running a node yourself, or an IP you have found on [Node Explorer](http://www.nodeexplorer.com/). Then press save.
![](/content/images/2015/05/Screenshot-2015-05-31-13-11-32.png)
 
**6)**	You should now see a green status bar at the top of your screen. This indicates that your NEM client is connected to a fully synchronized NEM node (NIS) and you are good to go! 
![](/content/images/2015/05/Screenshot-2015-05-31-13-11-44.png)

If this is the first time for you to use NEM on that computer, you will need to either import your [private key](http://blog.nem.io/getting-started-with-nem/) or recover a wallet you have [backed up](http://blog.nem.io/how-to-find-export-or-delete-your-wallet-and-address-book-file/).
