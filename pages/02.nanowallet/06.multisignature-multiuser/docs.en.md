---
title: 'Multisignature and Multi-User'
taxonomy:
    category:
        - docs
---

<font size=-1>Thank you Jabo for initially writing this guide.</font>

Multi-signature accounts are a powerful tool to have at your disposal but you need to use this tool with caution. Some important things to point out are:
 
* Once you convert an account to a multi-signature account, you can no longer initiate transactions from that account. All transactions from the multi-signature account must be initiated by one of the cosignatories. This can be thought of as a parent/child relationship.  The account(s) that are signers are parent accounts and the account that has been turned into a multisig account is a child account.  The parent accounts have full custodial control over the child account, and the child account no longer has any control over its funds. 
* NEM's current implementation of multisig is "M-of-N", meaning M can be any number equal to or less than N, i.e., 1-of-4, 2-of-3, 4-of-9, 11-of-12 and so on. NEM also allows "N-of-N" accounts, i.e., 1-of-1, 2-of-2, 5-of-5, 10-of-10 and so on.  With N-of-N accounts transaction have to have all N cosignatories sign the account, but to edit the singers on the account it is "N-1", meaning for example, if you create an account with 3 cosignatories only 2 signers are necessary to delete or change the third signature - hence N-1 (3 being "N" in the above example).
* You can create multi-signature accounts with up to 64 signatories. But beware, if more than 1 key gets lost this would currently result in the permanent loss of access to the funds held by the multi-signature account.

##### Tip
If you don't want to use any existing addresses as cosignatories, you can just create new accounts.