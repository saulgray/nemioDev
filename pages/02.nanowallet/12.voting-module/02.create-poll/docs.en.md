---
title: 'Create a Poll'
taxonomy:
    category:
        - docs
---

**How to Use the NEM Voting Module**

You will find two options on the services tab on NanoWallet: See Polls and Create Poll. Let’s walk through their features.

**Creating a Poll**

Example of a poll creation form on the testnet:
![](1-5ehVC2Lx2tsVEglO-4kGfg.png)

On the Create poll Option you will find a form with all the information needed for a poll to be created. There is a small description for each field.

The fields that define a Poll are:

* Title: Short Title people will see on the poll Index and when opening the poll.
* Description: The description’s purpose is to explain what the poll is about and to include relevant information. The description field is not required but it is strongly encouraged to include one, so people know exactly what they are voting on.
* Poll Index: The address of the Index Account to send the poll. By default a public one is set.
* Date of ending: The date and time the poll will end and no more votes will be counted.
* Multiple: you can choose if the vote will be multiple option. In this case vote weights will be split between the different options a voter chooses.
* Type: The type of vote counting (details below).
* Options: The options voters will be able to choose from.
* Whitelist: Only used for white list polls, where only votes from the given addresses will be accepted.
* When creating a poll the user can specify the way votes will be weighted. On the current version two options are offered:
* POI: Proof of Importance is a great tool for weighing the votes on polls, specially those that affect the NEM community. In the voting platform we make it possible to use the importance score, intrinsic to NEM, to weigh votes in a simple way.
* White List: On simple polls every vote counts the same. A whitelist is required for this polls since anybody can create as many NEM accounts as they want.
