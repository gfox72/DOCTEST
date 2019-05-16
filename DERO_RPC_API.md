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

1 Introduction</br>
  1.1 Data types</br>
  1.2 Code examples</br>
2 Quick Overview</br>
3 DERO Daemon RPC Interface</br>
  3.1 Introduction</br>
  3.2 Methods via POST</br>
    3.2.1 getblockcount</br>
    3.2.2 get_info</br>
    3.2.3 getblocktemplate</br>
    3.2.4 submitblock</br>
    3.2.5 getlastblockheader</br>
    3.2.6 getblockheaderbyhash</br>
    3.2.7 getblockheaderbytopoheight</br>
    3.2.8 getblockheaderbyheight</br>
    3.2.9 getblock</br>
    3.2.10 gettxpool</br>
  3.3 Methods via GET</br>
    3.3.1 getheight</br>
    3.3.2 gettransactions</br>
    3.3.3 sendrawtransaction</br>
    3.3.4 is_key_image_spent</br>
4 DERO Wallet RPC Interface</br>
  4.1 Introduction</br>
  4.2 Methods via POST</br>
    4.2.1 getaddress</br>
    4.2.2 getbalance</br>
    4.2.3 getheight</br>
    4.2.4 transfer</br>
    4.2.5 transfer_split</br>
    4.2.6 get_bulk_payments</br>
    4.2.7 query_key</br>
    4.2.8 make_integrated_address</br>
    4.2.9 split_integrated_address</br>
    4.2.10 get_transfer_by_txid</br>
    4.2.11 get_transfers</br>

# Chapter 1
## Introduction
This document describes the RPC API for the Dero daemon and wallet which are implemented
according to the JSON RPC 2.0 standard.
We will give a description of the available RPC methods with their parameters and results and
provide code examples for calling the methods and the data returned.
Dero is the first crypto project to combine a Proof of Work blockchain with a DAG (Directed
Acyclic Graph) block structure and wholly anonymous transactions. The fully distributed ledger
processes transactions with a twelve-second average block time and is secure against majority
hashrate attacks.
Dero will be the first CryptoNote blockchain to have smart contracts on its native chain without
any extra layers or secondary blockchains.
For more information visit http://www.dero.io

# 1.1 Data types
Dero is written in Go, so we give the data types of the parameters and results in Go format. It is
pretty straightforward to convert them to other languages.
Amounts in Dero have a resolution of 112 decimals and are handled as unsigned 64 bit integers.

`e.g. 1.5 Dero is encoded as 1500000000000`

As Dero combines DAG and Blockchain, it uses different height information than traditional
blockchains. Dero blocks have an additional height value, called the topological height.
The topological height is unique for each block, while at each blockchain height there can be
multiple blocks associated. Each blockchain height contains at least a main block and optional
side blocks.

<img align="center" src="/ASSETS/DEV1_1.png" width="320">

# 1.2 Code examples

The examples provided for each method are written in Python - using the ’request’ package to
build the HTTP request and perform the JSON encoding.

```
#construct payload for HTTP request
payload = {'jsonrpc': '2.0', 'id':'1','method': 'getblockcount'}

#send request
r = requests.post('http://127.0.0.1:20206/json_rpc', json=payload, headers ={'Connection':'close'})

#read response object
if (r. status_code == requests codes.ok):
  jsondata = r. json ()
  result = jsondata ["result"]

#Result of RPC call
# result={
# ’count’: 384982,15
# ’status’: ’OK’
# }
```




