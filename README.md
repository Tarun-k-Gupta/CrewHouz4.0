# Recover Vault Protocol Using ICP .
So if you haven’t notice , there isn’t a forget password button in web3 yet, and if there is it’s usually centralised
and trusted provider giving that service . But what if that wasn’t the case ? What if we could have a
decentralised trustless wallet recovery system powered by smart contracts ? Well this is what i propose here 

## Problem it solves
The Web3 Recovery Crisis Web3's foundational security model creates a critical user experience flaw: unlike traditional systems, wallets force users to memorize irreplaceable seed phrases with no true "forgot password" alternative. Lose your phrase, and your assets are permanently lost. Current recovery "solutions" like Near and TON wallets attempt to bridge this gap but function as centralized honeypots – as demonstrated by Near's 2021 breach where compromised email servers led to thousands of drained wallets. Alternative approaches like MPC wallets reintroduce trusted operators (making them partially custodial), while social recovery mechanisms depend on friends or DAOs, sacrificing both scalability and privacy. This creates an unacceptable trade-off: users must choose between absolute self-custody (with permanent loss risks) or recoverability (with centralized vulnerabilities). Our protocol shatters this compromise by enabling truly decentralized recovery – delivering both ironclad self-custody and seamles

## Project Decription
A decentralized, non-custodial wallet recovery protocol built on the Internet Computer (ICP). It uses DKIM email signatures and smart contracts to let users securely recover lost seed phrases via their own email—without trusting any third party.

## Current Solutions 
In 2021 , Near wallet did implement this , they used a centralised OTP email server to do that, plus the private
key was stored by them encrypted in their server. Soon enough a social engineering attack , comprosed the
email server and thousands of customer wallets were compromised . Ton wallet currently is doing the same
thing , and hence are not a non custodian wallet option. Then there are MPC wallets , MPC wallets could be
seen as partially custodial and non interoperable with normal wallet standards . Hence MPC wallets do require
a central party to be there

## How it works ?
We use DKIM signature verification to verify emails , and vet keys to store end to end encrypted seed phrases
. The Encrypted seed phrase can only be decrypted if the user sends a valid DKIM signature of this email .
Hence we can now have wallet recovery mechanism
## Flow Of Protocol
### User Registersing 
1. User clicks on register which shows 5 digit number that is going to expire in 5 minutes
2. Then an instruction is set out such that the user has to give a copy of the email which has those 5 digits
3. Then the user sends an email to the email he want to use as recovery.
4. Then submits the copy of the email from his recovery email
5. Then user enters the secret phrase
### User Retrieving Secret
1. User enters email
2. After checking if the email is registered , then a 5 digit number is show
3. The user sends the copy of a email which has those 5 digit number
4. The smart contract verifies the email using DKIM and return the phrase

## DEMO !
Click to view video
[![Demo Quick Video](https://youtu.be/Bc1x_d5B6ro)]

## Link
Backend canister via Candid interface:

app_backend: https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=ckuxw-iiaaa-aaaac-awwfq-cai

dkim: https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=c7tg3-jaaaa-aaaac-awwga-cai

system_api: https://a4gq6-oaaaa-aaaab-qaa4q-cai.raw.icp0.io/?id=cysap-eyaaa-aaaac-awwgq-cai


