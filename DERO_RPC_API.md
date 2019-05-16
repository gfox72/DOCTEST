---
category: DEV
ref: 1
title: DERO ATLANTIS RPC API
author: Captain
created: 2018/9/4
status: DRAFT
version: 2.0
---

<img align="right" src="/ASSETS/DERO_LOGO_320x320.png" width="80">
</br>
</br>

# CORE-1: DERO ATLANTIS RPC API V2.0

## Table of contents

1 Introduction
  * 1.1 Data types
1.2 Code examples
2 Quick Overview
3 DERO Daemon RPC Interface
3.1 Introduction
3.2 Methods via POST
3.2.1 getblockcount
3.2.2 get_info
3.2.3 getblocktemplate
3.2.4 submitblock 
3.2.5 getlastblockheader
3.2.6 getblockheaderbyhash
3.2.7 getblockheaderbytopoheight
3.2.8 getblockheaderbyheight
3.2.9 getblock
3.2.10 gettxpool
3.3 Methods via GET
3.3.1 getheight
3.3.2 gettransactions
3.3.3 sendrawtransaction
3.3.4 is_key_image_spent
4 DERO Wallet RPC Interface
4.1 Introduction
4.2 Methods via POST
4.2.1 getaddress
4.2.2 getbalance
4.2.3 getheight
4.2.4 transfer
4.2.5 transfer_split
4.2.6 get_bulk_payments
4.2.7 query_key
4.2.8 make_integrated_address
4.2.9 split_integrated_address
4.2.10 get_transfer_by_txid
4.2.11 get_transfers


