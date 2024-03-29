---
description: >-
  EVER Wallet has a very convenient seed phrase, keys and accounts management
  structure.  You can freely add them to your EVER Wallet for further use.
---

# Architecture

## [Seed](seed-phrase-management/)

At the head of the architecture is **Seed**.

A seed phrase is a series of words generated by your cryptocurrency wallet that gives you access to the cryptocurrency associated with that wallet. Think of the wallet as a cryptocurrency password manager and the seed phrase as a master password. As long as you have the seed phrase, you will have access to all cryptocurrencies associated with the wallet that generated the phrase, even if you delete or lose the wallet.\
\
&#x20;**If you lose your seed phrase you lose access to your tokens!**

## [Public key](keys-management/)

The public key is the repository of your accounts. \
Each public key can be associated with one account of [each type](../getting-started/install-and-singing-in/types-of-account.md). \
The public key is needed when creating a [Multisig wallet](../multisig/) - it is its address that is entered as a custodian during its [deployment ](../multisig/creating-a-multisig-account.md)and a request to confirm the transaction will be sent to it.

## [Account](account-management/)

Accounts are the bottom step in this architecture. \
The account allows you to [send ](../manage-assets/sending-and-receiving-tokens.md#sending)your tokens, as well as store and [recieve](../manage-assets/sending-and-receiving-tokens.md#receiving) them. \
It is the account address that you specify when you want to [send tokens to any network member](../manage-assets/sending-and-receiving-tokens.md#sending) and [vice versa](../manage-assets/sending-and-receiving-tokens.md#receiving).\
