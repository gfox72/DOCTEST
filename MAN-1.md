---
category: MANUAL
ref: 1
title: CREATE, BACKUP AND RESTORE A DERO WALLET
author: gfox
created: 2018/02/18
status: DRAFT
---

<img align="right" src="/ASSETS/DERO_LOGO_320x320.png" width="80">
</br>
</br>

# MAN-1: CREATE, BACKUP AND RESTORE A DERO WALLET

## Table of contents
1. [Introduction](#req)
2. [Create a wallet](#create)
3. [Syncing your wallet](#using)
3. [Back up a wallet](#backup)
4. [Restore a wallet](#restore)


## Introduction<a name="req"></a>
A wallet allows you to manage your DERO funds, it allows you to intiate or consult transactions, view balance and consult the security related information.  
Pre-compiled DERO wallet binaries are available for most common operating systems (ARM, INTEL, MAC, Windows, FreeBSD, OpenBSD, Linux etc) and can be downloaded from [the Dero Github](https://github.com/deroproject/derosuite/releases). 
These wallets are so called CLI (Command Line Interface) applications which are intended to be run in a terminal or shell window. This manual assumes you are familiar with basic navigation and running applications on your specific OS.

## Creating a wallet<a name="create"></a>
Start by downloading the appropriate binary for your operating system and unpack the file to a folder of choice (but one that you will easily remember once you need it !).
Once unpacked you will typically find 3 files in your folder:
<img align="left" src="/ASSETS/MAN-1/DERO_WALLET_UNPACK.png" width="320">
</br></br></br></br>

To create and access your wallet, you will be using the *dero-wallet-cli* file (name may vary with OS version).

Navigate to the folder which contains your DERO wallet files and execute the dero-wallet-cli application, this should give you a terminal window showing some version info and then the DERO wallet menu.
<img align="left" src="/ASSETS/MAN-1/DERO_WALLET_MENU.png" width="480">
</br></br></br></br></br></br></br></br></br></br></br>

As shown in the next image, select option 2 (2+enter) to create a new wallet, you will be promted to provide a wallet name.
As you will be able to create multiple wallets, make sure the naming of your wallet is a clear and unique identifier allowing you to easily remember/retreive it in case you haven't used in for a while. In our example below we chose dero_test.db (we added the .db extension explictly). Upon entering the name, you will be prompted to provide a password to access your wallet, again make sure this is something you will remember later. As you enter keystrokes the number between brackets will show how many characters you have entered. After entering the password and confirming it, you will be asked to select your preferred language for the wallet interface, in our example we selected English by entering 0.

<img align="left" src="/ASSETS/MAN-1/DERO_WALLET_CREATE.png" width="480">
</br></br></br></br></br></br></br></br></br></br></br>

Once you provided this information and selection of language, your wallet will be created. In case a technical issue would prevent you to use or retrieve your wallet file, you can restore it from the blockchain by using a so called SEED. A SEED is a set of 25 words which **allows to obtain full access to your wallet funds so as stated by the interface, write them down and store them in a safe place.** The SEED in the example above starts with the words *argue nylon tamper* etc.  

You have now created your wallet file ready for use, see next step how to sync your wallet.

:exclamation: To stop using your wallet, it's advised to close the application by selecting 0 from the menu, this will allow the application to store its last state before shutting down.

:exclamation:Your wallet file location may vary depending on your operating system or configuration, it's advised to do a system search on the wallet name so you know where your file is situated.

## Syncing your wallet<a name="syncing"></a>

Now that you have created your wallet, you will open it by running the dero_wallet_cli application and providing your wallet file name and password. To have your wallet show your funds, it is required to have it syncronized with the DERO blockchain.
As shown in previous image at the bottom left, the sync status will be shown by 2 numbers separated by a /.

As the DERO wallet application itself does not sync with the blockchain, there are 2 options to make it sync: 

### Syncing with a local copy of the DERO blockchain
If you prefer to keep and sync your wallet with a local copy of the DERO blockchain you will have to prepare for downloading a substantial amount of data which will be over 25Gb in size (at time of writing this document). **Running and connecting to your own Derod daemon is the most safe and secure way for doing transactions on Dero's Blockchain.** To download and gather all this data locally, you will use the *derod* application next to the *dero-wallet-cli* application. Once you start the *derod* application (naming may vary based on OS system), it will start to sync with the blockchain. The total time to download and sync your wallet depends on network connection and harddrive technolgy, SSD drives speed up things significantly while with traditional HDD it may take a few days to do the full sync.

<img align="left" src="/ASSETS/MAN-1/DERO_DAEMON.png" width="480">
</br></br></br></br></br></br></br></br></br></br></br>

As shown in the above picture, the *derod* application will provide some basic information on it's version and file locations (daemon data directory being the one where the blockchain will be stored). The sync progress is shown at the left bottom, in our example it is showing 2592980/3519905 [2628334/3562862]. The numbers between the square brackets show the current DERO blockchain block height and the numbers in front indicate the local blockchain sync height. Until these numbers are identical, your wallet is not fully synced and may not show correct balance.

### Syncing with a remote node
If you prefer not to download and keep the full blockchain on your system, you can opt to connect to a so called remote node. To do so, you will start the wallet application with some additional command parameters which is something you can best do via a terminal or shell window (depending on your OS). The parameter to start your wallet application with and have it sync with a remote node is *--daemon-address=https://rwallet.dero.live*. Newer versions of the wallet allow you to do this with the parameter *--remote*.
 











