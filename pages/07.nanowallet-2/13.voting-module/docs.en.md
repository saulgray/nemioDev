---
title: 'Voting Module'
taxonomy:
    category:
        - docs
---

Thanks to the NEM Voting Module anyone can create and participate in polls using Blockchain technology.

The NEM voting platform is a new NanoWallet module that allows anybody to create and vote on polls stored on the NEM blockchain. The vote counting is made by the client with open source code, so that it is completely transparent. All the information is publicly available to everybody.
NEM is ideal for a voting system due to the importance score inherent to every account on the network, which provides a very interesting way to weight votes.

Technical Details

Account Structure of The module. Colored arrows are messages.
![](https://cdn-images-1.medium.com/max/1600/1*kQh38bgPVUgQ1XUeZwpcMg.png)
There are 4 main concepts on the data structure of the module:
Poll Index Account (PI)
Poll Account (PA)
Option Account (OA)
Voter Account (V)
When a poll is created the first thing that happens is the creation of a Poll Account. Then the creator sends all the poll information to the Poll Account as messages in NEM transactions. This information includes things like the Title, the type, the description, etc.
Next, an Option Account is created for each of the options the poll has. A message is then sent to the Poll account containing the addresses of all the Option Accounts, together with their description.
If the previous steps have succeeded, now the poll is correctly formed and can be already voted on, but first we will add it to a Poll Index. This is done by sending the Index Account some information abut the poll, but not all, so that it can be loaded faster. We call this the poll header, and it contains the address of the Poll Account, the title, the type, etc.
Now, after waiting for the message confirmations, the poll Is correctly formed and can be displayed and found on the poll Index. You can now Vote on it.
Votes are sent as an empty NEM transaction to the chosen option account. The transaction doesn’t send any xem or message, the cost of a vote is simply the fee (1 xem for normal votes, 7 xem for multisig votes).
Anybody can create a new Poll Index. When creating a Poll Index a new NEM account is created, and two messages are sent by the creator. The first message is to the poll Index, declaring it as such and sending information to it. Poll Index information says if it is a private index, and if it is, then it has the address of the creator. The second message is sent to the creator account from itself containing the Index’s address, so that a user can find all the polls created by him/herself looking at the self-sent messages.
Private Indexes can be created, where only the creator of the index Account can submit polls, and when seeing the poll list from such an index, all polls not created by the Index owner will be ignored.
While the voting is still ongoing a temporary result is calculated pulling data from the current block in the blockchain. Once the poll ends the result is calculated from historical blockchain data.
Additional Comments
We want to implement another type of vote counting in the future which will use mosaics to weight the votes. This would introduce very interesting ways to create votes, for example if you have a company and you want to have an internal vote you can create a mosaic and distribute it. You could even send more mosaics to more important figures on the company. You could also have POS counting by using xem as the mosaic.
We have this functionality working with ongoing polls, so that you can weigh the votes on the current moment. But since historical data for mosaics is not yet accessible by the NEM API, we decided against including it on the first version, since we can’t have past voting and you wold have to trust a result saved in the past instead of calculating it from the blockchain.
We prefer to wait until we can make it fully trust-less and decentralized.
Special thanks to the whole Atraura team for helping with the development of the project, specially Albert Castellana who got me into NEM and guided me on my first steps on this promising technology. Also Jeff McDonald who provided me with feedback and encouragement. I would also like to thank all the testers who found bugs and provided feedback, like Rin Mizunashi and Quantum Mechanics. This would have not been possible without them.