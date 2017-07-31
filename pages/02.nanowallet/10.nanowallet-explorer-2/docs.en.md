---
title: 'Nanowallet Explorer 2'
taxonomy:
    category:
        - docs
---

You will learn how to activate and start delegated harvesting in NanoWallet. Additionally, you will learn two ways for harvesting.  These are delegated harvesting on a remote server provided by somebody else, or learning how to use delegated harvesting by running a local NIS yourself.

**To activate and start delegated harvesting in NanoWallet you need a [XEM Account](https://blog.nem.io/how-do-i-get-importance-on-the-nem-blockchain/) with at least a 10'000 XEM vested balance.**
To check how long it takes for you to get a vested balance of 10'000 XEM, you can use [this](http://samesake.com/xem/harvesting-calculator/) harvesting calculator.

## Activation
Before you can start delegated harvesting, you need to activate it. Consider this to be the same thing as registering on the blockchain that you want to harvest. To do so go to "Services - Manage delegated account" and activate it from the left panel by entering your password and clicking "Send".   

Activation takes ~6 hours and will cost you 6 XEM in fees. **Activation only needs to be done one time per account.**
![activate delegated account](http://imgur.com/IjYaY2O.png)
To check if delegated harvesting is active take a look at the right panel:

![inactive](http://imgur.com/WZcLKvC.png)
"Remote status" will change to active after 6 hours:
![active](http://imgur.com/O30RjPB.png)
Once your "Remote status" is active, you can continue with the next step.

## Start / Stop
Now that the "Remote status" is active you need to wait until "Vested balance" (right next to "Remote status") shows at least 10'000 XEM.

![vested](http://imgur.com/yIPI2t2.png)
If this is the case, you can start delegated harvesting from the panel below.

Enter your password, choose a node and press on the "play icon" to start it. 
![play](http://imgur.com/HABqSr3.png)
If everything is successful, the "play" icon will change to a "stop" icon.

![play](http://imgur.com/BKvKeoS.png)
If you receive an error, it is most likely because the node you selected is already full. Every node only has a certain amount of harvesting slots, and once they are full, you will need to choose another node.

One way of finding another node is to open [supernodes.nem.io](http://supernodes.nem.io) and try different nodes from the provided list. 

Another way to find nodes with free harvesting slots is the @NemNotificationsBot on Telegram. With the command /harvestingSpace it will provide you nodes with free slots. Read more about it [here](https://blog.nem.io/nem-chain-supernode-notifications-telegram-bot/).

**Check your NanoWallet from time to time to see if harvesting is still ongoing. If the node you have selected restarts, you also have to start harvesting again! Meaning, as long as the node was on, it will continue to harvest for you for free, but if it reboots, you will have to request it to harvest for you again.**

## Local NIS
Above we showed how to harvest on a remote node, and it is a normal case for many that they run delegated harvesting on a remote NIS, but it is also possible to run delegated harvesting on a local NIS. The advantage of this is that you will always know that your account is being harvested on and you won't have to rely on others. 

**NIS needs Java 8 64 bit to run. Download it from [java.com](https://www.java.com/en/download/manual.jsp) and install it with default values.**

To run a local node, download and extract the standalone client from [nem.io](https://www.nem.io/install.html) or [the developer's repository](http://bob.nem.ninja/). 

In the extracted folder (nis-ncc) you will find a file called "runNis" (Windows: runNis.bat, OSX/Linux: nix.runNis.sh).
![runnis](http://imgur.com/bWxx446.png)
Windows: Execute the file by double-clicking it
OSX/Linux: Open a terminal, navigate to the folder "nis-ncc" and execute "nix.runNis.sh"

![NIS terminal](http://imgur.com/Kyxq1JQ.png)

Once NIS runs, let it run for 1-2 minutes and stop it. We do this to let NIS create the needed folder structure.
Navigate to the created folder structure.
Windows: C:\users\username\nem\nis\data
OSX/Linux: username/nem/nis/data

![folder location](http://imgur.com/AxmeKzJ.png)

Delete both files (NIS needs to be stopped to delete the files).
Navigate to [bob.nem.ninja](http://bob.nem.ninja) and download the DB file. We do this to speed up the initial sync of NIS.

![bob.nem.ninja](http://imgur.com/OgDXINY.png)

After the download completes, extract the file "nis5_mainnet.h2.db" and place it in the folder from above.

![db](http://imgur.com/07BRFsT.png)

Once you have done this, start NIS again with "runNis" and let it run in the background. NIS will now finish syncing. 

To check if it is synced, you can open [alice6.nem.ninja:7890/chain/height](http://alice6.nem.ninja:7890/chain/height) in a web browser.

![alice6 chain height](http://imgur.com/wsHNbpH.png)
Open [localhost:7890/chain/height](http://localhost:7890/chain/height) in another web browser window to compare the block height to alice6 (localhost needs to be **at least** at the same block height as alice6).

![localhost chain height](http://imgur.com/tSPBSmV.png)
When NIS is synced click on the "Node" option in the top bar of your NanoWallet and enter "localhost" in the "Custom node" field:

![select localhost nanowallet](http://imgur.com/FOCnNnL.png)

Click "+" to select localhost. It should look like this:

![localhost selected nanowallet](http://imgur.com/bAxJYKP.png)

After that close the node settings. 
You are now connected to your local NIS!

**Remember to let NIS run in the background!
To start delegated harvesting with your local NIS repeat the steps from above but select "localhost" in the "Start/Stop delegated harvesting" panel for your node.**


## Review Blocks Created
You can later log in to the Dashboard of your NanoWallet and get a summary of the latest blocks and fees you have collected. 
![checking your collected fees](http://i.imgur.com/JY8LbwQ.png)


*The NEM Team would like to thank Patrick (Telegram: @Spizzerb) for contributing this blog.*


