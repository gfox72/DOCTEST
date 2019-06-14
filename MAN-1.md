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
3. [Back up a wallet](#backup)
4. [Restore a wallet](#restore)


## Introduction<a name="req"></a>
A wallet allows you to manage your DERO funds, it allows you to intiate or consult transactions, view balance and consult the security related information.  
Pre-compiled DERO wallet binaries are available for most common operating systems (ARM, INTEL, MAC, Windows, FreeBSD, OpenBSD, Linux etc) and can be downloaded from [the Dero Github](https://github.com/deroproject/derosuite/releases). 
These wallets are so called CLI (Command Line Interface) applications which are intended to be run in a terminal or shell window. This manual assumes you are familiar with basic navigation and running applications on your specific OS.

## Creating a wallet<a name="create"></a>
Start by downloading the appropriate binary for your operating system and unpack the file to a folder of choice (but one that you will easily remember once you need it !).
Once unpacked you will typically find 3 files in your folder:
<img align="left" src="/ASSETS/MAN-1/DERO_WALLET_UNPACK.png" width="480">

To create and access your wallet, you will use the dero-wallet-cli file.
To have your wallet sync with the DERO network, you will use the derod file (DERO Daemon).

Navigate to the folder which contains your DERO wallet files and execute the dero-wallet-cli application, this should give you a terminal window showing some version info and then the DERO wallet menu.
<img align="left" src="/ASSETS/MAN-1/DERO_WALLET_MENU.png" width="480">







## Who does what ? <a name="whoDoesWhat"></a>
The Dero project involves several groups of people interacting with eachother:
  * **Core** development team : develops technology and master all the technical knowhow
  * **Staff** members : interact with Core development team and perform specifc trusted functions such as moderator, marketing, documentation
  * Community Advisory Board members (**DCAB**) : represent the community and consolidate suggestions or concerns
  * Community members : users, investors, developpers, enthousiasts
  * **Stargate** testers : developpers

Assignment of these roles is done by Dero Staff members (mostly moderators) and identification via means of tagging on the Dero discord.

For documentation creation and management, there is a lead Staff member working with DCAB members to:
  * Establish document management strucutre tailored to the project needs and its users
  * Align and standardize on formatting
  * Prioritize document creating
Once the document management structured is established and standardization and formatting are proven to work efficiently, more involvement 
from the community will be encouraged and facilitated to make Dero's documentation decentralized and a best in class reference for its users.

## Document categories<a name="docCat"></a>
As the project grows, decisions on different document types may evolve in function of the demand from its community and individuals developping on the Dero blockchain. Currently, the following categories are considered required to start with:
  * DIP : Dero Improvement Process documents - see DIP-1 for reference
  * INFO : Informational and guidelines (as this very document)
  * APP : Application notes demonstrating technical possiblities
  * WP : Whitepaper or variations thereof
  * SPEC : Specifications
  * TECH : Technical information on the DERO project and features
  * DEV : Developper documentation
  
## Documentation workflow <a name="docWorkflow"></a>
Requests for documentation (creation or editing) can originate from many different sources and require to be channeled so they can be filtered/vetted, 
prioritized and directed to document authors, approved and published. 

`source of request > documentation lead > document creation by author > approval by doc lead  > publish`

## Design guidelines <a name="docDesign"></a>
Following design guidelines apply to all types of documentation and are to be applied by document authors:

Each document should be written in markdown format and start with a header as descrived also in DIB-1 which will provide a table structure 
at top of the document:
> `---` </br>
> `category:`</br>
> `ref:`</br>
> `title:`</br>
> `author:`</br>
> `created:`</br>
> `status:`</br>
> `---`</br>

Then, the DERO logo should be used:
> `<img align="right" src="/assets/DERO_LOGO_320x320.png" width="80">`</br>
> `</br>`</br>
> `</br>`</br>
Mind that as for the logo insertion, all images should be referenced relative to the document root, under a folder /assets

Then, the title of the document, using # to make a heading. An example:

> `# DIP-1: DIP Purpose and Guidelines`

After the document title, there should be a table of contents.

> `## Table of contents` </br>
> `1. [Chapter1](#link1)` </br>
> `2. [Chapter2](#link2)` </br>
> `3. [You get the point](#link3)` </br>

Then the first reference/chapter with the link used for the table of contents or reference within the document:
> `## Chapter 1 <a name="link1"></a>`

For formatting you can reference the [general markdown syntax for github](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) but hereafter some quick examples of the most commonly used ones:

`**bold text**`gives **bold text**</br>
` * first bullet`gives a bullet like below</br>
  * first bullet

`    * second bullet`givess a secondary bullet like below</br>
    * second bullet
    
:exclamation: This document itself can also be reviewed for most common MD syntax.