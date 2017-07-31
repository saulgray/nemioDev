---
title: 'Namespaces and Mosaics'
taxonomy:
    category:
        - docs
---

[Deutsch](https://forum.nem.io/t/how-to-make-your-first-namespace-and-mosaic/3898/2)

This guide will cover the basic setup of namespaces and mosaics in the NanoWallet.

To create a namespace you need:
- 5000 XEM for the root namespace
- 200 XEM for every subnamespace
 
To create a mosaic you need:
- 500 XEM

## Example 
You are a farmer with 50 potato fields. Since 50 fields are too many for yourself, you start to think about selling some of the fields to investors. 

How can this be done with NEM and NanoWallet?
With namespaces and mosaics of course...

## Creating a namespace
### Introduction
Before we create a mosaic to represent the 50 fields, we need to create a namespace and we will also create a sub-namespace. For this example, we create a root-namespace for the farmer and a sub-namespace for the potato fields.

A root-namespace can be compared to a web domain, for example, nem.io. 
A sub-namespace can be compared to a sub-domain such as blog.nem.io.

**Following namespaces have to be created:**
Root-namespace: farmer
Sub-namespace: potato (farmer.potato)
### Creation of root- and sub-namespaces
Login to the NanoWallet, go to Services and choose "Create namespace".
First, we create the root namespace.
![create namespace](http://imgur.com/ReVopg1.png)
- Parent Namespace: select ". (New root Namespace)"
- Namespace: farmer (this is the name of the namespace)
- Password: Your wallet-password

Once you have entered the values, click "Register". Go to the Dashboard and check, if the registration was successful:
![create namespace](http://imgur.com/caUyzq1.png)

Now that the root-namespace exists, we can create a sub-namespace.
![create namespace](http://imgur.com/36c2quM.png)
- Parent Namespace: select "farmer"
- Namespace: potato (this is the name of the sub-namespace)
- Password: Your wallet-password

Once you have entered the values, click "Register". Go to the Dashboard and check, if the registration was successful:
![create sub-namespace](http://imgur.com/Mf8gous.png)
## Creating a Mosaic Asset
After the creation of the Namespaces, we move on to create a mosaic for the 50 potato fields.
![create mosaic](http://imgur.com/Vx7prpZ.png)
**Mosaic definition**
- Parent Namespace: select "farmer.potato"
- Mosaic name: field (this is the name of the mosaic)
- Description (optional): a short text description 
- Password: Your wallet-password

**Mosaic properties**
- Initial supply: 50 (50 fields)
- Divisibility: 0 (fields are not divisible)
- Transferable: Means, the mosaic is transferable
- Mutable supply: Means, the supply can be changed up or down in the future

Once you have entered all the values, click "Send". Go to the Dashboard and check, if the creation was successful.
![mosaic creation](http://imgur.com/cty3uGG.png)

If you open the "Explorer", you can see that you now own 50 assets of farmer.potato:field
![mosaic creation](http://imgur.com/nRAcMZ2.png)

## Transfer of Mosaic
### Introduction
Everything is set up now and you are ready to sell your first field(s) to investors. Since you are using NEM to manage your fields, your investors also need to set up a NEM NanoWallet. Once done, they can send you their account address.

### Transfer (farmers view)
Investor 1 (Alice) has set up the NanoWallet and wants to buy **2 fields** from you. 
The account address from Alice is: TC2S7V-55FISZ-BJJBP4-UZUDTO-X42P7O-H5WJET-NU4A

To send 2 fields to the account, go to Send in NanoWallet and choose "Mosaic transfer":
![mosaic transfer](http://imgur.com/Rgmyj5j.png)
Remove the "nem:xem" mosaic:
![mosaic transfer](http://imgur.com/ZiNa8zF.png)
Choose "farmer.potato:field" from the "Currency" dropdown and click "Attach":
![mosaic transfer](http://imgur.com/YUzaQKa.png)
Add the account address from Alice in the "To" field. Set the amount for the field(s) on the right side, enter your wallet-password and click "Send":
![mosaic transfer](http://imgur.com/4fGZILQ.png)
Once you have sent the mosaic asset(s), go to the Dashboard and check, if the transfer was successful:
![mosaic transfer](http://imgur.com/P6Y4Peg.png)

### Transfer (investors view)
Alice will see the incoming transactions on her Dashboard:
![mosaic transfer](http://imgur.com/YjtsmAu.png)
To check all her owned mosaics, the investor can open the Explorer:
![mosaic transfer](http://imgur.com/ptzfdD9.png)

## Change of supply
Your business runs great, in fact, you are thinking about adding another 50 potato fields to your farm. 
How to add those new fields to your Mosaic?
Go to Services - "edit mosaic":
![mosaic transfer](http://imgur.com/Gxg1isV.png)
- Select mosaic: farmer.potato:field
- Change type: create 
- Change amount: 50

Check the resulting supply for errors and click "send." Done.

## What about the tomatoes?
Since the potato field business is running great, why not do the same to the tomato fields? 
Since you already have your root-namespace you can create a sub-namespace, for example, "farmer.tomato" and create a mosaic for it just like you did for the potato fields (farmer.tomato:field). Customers happy with your potato asset can now trust your tomato asset too, as they could have both only been created by you. 

*The NEM Team would like to thank Patrick for this blog.* 
 
