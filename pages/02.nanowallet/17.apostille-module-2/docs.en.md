---
title: 'Apostille Module 2'
taxonomy:
    category:
        - docs
---

## Introduction
"A blockchain notarization and timestamping service with transferable, updatable, branded, and conjointly owned notarizations. The Apostille system’s key innovation is taking data which represents an underlying person, place, or thing and giving that data its own private key derived deterministically from its contents. This is used to create an account that represents the state of that object. These are dynamic accounts that can be used to prove authenticity, show ownership, and record updates, as well as be branded, transferable and conjointly owned. " 
_- Apostille white paper_

no·ta·rize (nō′tə-rīz′) To certify or attest to (the validity of a signature on a document, for example) as a notary public.

One can easily conclude from the texts above that NEM's Apostille service is used for notarizing and checking the authenticity of files notarized on the NEM blockchain. Its uses are various, but one big one is to register important documents that need a certificate of origin and content. NEM happily provides these in a .zip file after a successful notarization, containing a .pdf of the certificate (apostille) along with the original file with a hash in its filename and updated .nty file which is your notarization history.

It's easiest to learn from examples so I would like to start with one of many possible uses of the NEM Apostille service.

## The Problem with the Old System
The notary services in the real world, like a Notary Public verification, are highly useful for providing independent verification of important documents. Having a document notarized with a Notary Public's seal is the same as swearing under oath in court -- you're attesting that the facts contained in the document are true.

## What is Traditionally Needed for a Document to be Notarized?
To have a document marked with the Notary Public seal, you'll need to do the following: 
* Two pieces of identification (government issued photo ID and another one with at least your name) * Verbal agreement in front of the Notary that you understand and can attest to the facts of the document * Sign the document with the Notary as a witness * The Notary will then affix their stamp to the document * The document is now notarized
Simple, yet effective in providing proof and verification.
## Is There a Better Way?
At a fundamental level, what's really needed for a document to be notarized? 
* Irrefutable proof that you are who you say you are (government backed ID) * An independent and trusted third party to witness your signature (government backed notary service) * A stamp of approval by the third party
If you think about how a Notary Service works, it seems silly that this is the best we can do to verify important documents in the age of digital ubiquity and convenience. Each notarized document charges a significant fee, and the cumbersome task of physically getting it notarized can be daunting. However, until recently, it was very difficult to have something verified by an independent third party in the digital space.

## Enter the Blockchain
Bitcoin ushered in the breakthrough technology of the blockchain. The problem for many years, was to establish trust between two parties without an independent, reputable third party present. This was a roadblock for many industries and there was always a need to have a centralized middleman, extracting fees for their service as a witness (think Uber, AirBnB, Notary services).
One of the core functionalities of the blockchain involves historical immutability -- the inability to change past records once it's been verified. This breakthrough solution in the digital space has immense value and it's beginning to propagate across many industries.

## The Apostille Way
Apostille is a more robust notarization service built on top of NEM's blockchain. Apostille seeks to provide all of the functionalities inherent in traditional notary services, which includes verifiability, transferability, and updatability, by taking advantage of NEM's naming service, multi-signature accounts, messaging and blockchain assets (mosaic). With Apostille on NEM, new 2.0 notarizations are possible that provide far more feature and functionality than anything before. Now notarizations are not just one-off timestamps, but instead become proof of notarizations that are updatable, brandable, contain third party memos and verifications, and can even be transferable. The result is an ever-changing notarization to reflect the ever-changing real world.

## Why Notarize Files?
**Use Case: Patent**
You are an inventor, and you are discussing financing terms about your patent application with third parties. Each of them requires a technical draft, but you’re skeptical of them stealing your ideas. You sign some confidentiality agreements, but you’re still weary that these third parties can find a loophole to ransack your patent. You want something ironclad to prove without a doubt, that the exact specifications of your idea existed at a certain point in time. You turn to the NEM blockchain to use their Notary 2.0 service, Apostille. You notarize the PDF draft and embed in it the facts pertaining to your ownership of this idea, the confidentiality agreement between you and your parties, your technical specifications, and anything else that you believe will help you should somebody try to steal your idea.

By submitting these items to NEM’s Apostille, you have just recorded the state of the file (the original patent specifications), its timestamp, your name as the owner, and perhaps other co-signers to attest to the validity of the information. You can now have full confidence that this information is forever stamped onto NEM’s blockchain with all of the provided information, and you now have irrefutable proof that you were indeed the owner of this exact document at that point in time.

Now, if your malicious third parties were to edit this file that you sent them in any way, NEM’s Apostille audit service will know, and the file will fail the audit check.

As long as you hold the first notarization of the file and the file itself to audit it, you have absolute proof of ownership.