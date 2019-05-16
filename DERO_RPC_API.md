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

<img align="center" src="/ASSETS/DEV1/DEV1_1.png" width="800">

# 1.2 Code examples

The examples provided for each method are written in Python - using the ’request’ package to
build the HTTP request and perform the JSON encoding.

```python
#construct payload for HTTP request
payload = {'jsonrpc':'2.0','id':'1','method':'getblockcount'}

#send request
r = requests.post('http://127.0.0.1:20206/json_rpc', json=payload, headers ={'Connection':'close'})

#read response object
if (r. status_code == requests.codes.ok):
  jsondata = r.json()
  result = jsondata["result"]

#Result of RPC call
# result={
#  ’count’: 384982,
#  ’status’: ’OK’
# }
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example in python*

```curl
curl -X POST http://127.0.0.1:20206/json_rpc -d'{"jsonrpc":"2.0","id":"1","method":"getblockcount"}'-H'Content-Type: application / json'
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example in Curl*

# Chapter 2
## Quick Overview
  
| Method     | Section           | Description  |
| ------------- |:-------------:| ----- |
| getblockcount | 3.2.1 | Returns the currently synced height of the chain |
| get_info | 3.2.2 | Returns various info about the daemon and network |
| getblocktemplate | 3.2.3 | Return a block template (used for mining a block) |
| submitblock | 3.2.4 | Submits a mined block to the network |
| getlastblockheader | 3.2.5 | Returns the latest blockheader of the currently synced height |
| getblockheaderbyhash | 3.2.6 | Returns a blockheader from its hash |
| getblockheaderbytopoheight | 3.2.7 | Returns the blockheader from given topoheight |
| getblockheaderbyheight | 3.2.8 | Returns the blockheader from given height |
| getblock | 3.2.9 | Returns a block from its given hash |
| gettxpool | 3.2.10 | Returns a list of all the pending txhashes in the mempool |
| getheight | 3.3.1 | Returns the currently synced height and topoheight of the chain |
| gettransactions | 3.3.2 | Returns the specified transactions from either the blockchain or mempool |
| sendrawtransaction | 3.3.3 | Send a raw transaction to the network |
| is_key_image_spent | 3.3.4 | Checks if one of the supplied key images has been spent |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Daemon RPC methods*
  
| Method     | Section           | Description  |
| ------------- |:-------------:| ----- |
| getaddress | 4.2.1 | Return wallet address |
| getbalance | 4.2.2 | Return wallet balance |
| getheight | 4.2.3 | Return wallet height |
| transfer | 4.2.4 | Send Dero to another wallet address |
| transfer_split | 4.2.5 | Same as transfer |
| get_bulk_payments | 4.2.6 | Return payments with requested paymentIDs and filtered by height requested |
| query_key | 4.2.7 | eturn seed or view key |
| make_integrated_address | 4.2.8 | Generate integrated address with specified payment IDs |
| split_integrated_address | 4.2.9 | Split integrated address into standard wallet addressand payment ID |
| get_transfer_by_txid | 4.2.10 | Get transfer information by ID |
| get_transfers | 4.2.11 | Get all out/ingoing transactions from a wallet |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Wallet RPC methods*
  
# Chapter 3

## DERO Daemon RPC Interface

# 3.1 Introduction
When launched, the Dero daemon automatically starts the RPC server interface at port 20206.
You can change the port by using the rpc-bind parameter:
`.\ dero - wallet - cli . exe --rpc - bind =127.0.0.1:20206`

# 3.2 Methods via POST
Most RPC methods work by issuing HTTP POST requests and sending the parameters in the
payload.

```` python
# construct payload
payload = {'jsonrpc':'2.0','id':'1','method':'getheight'}

#send request
r = requests.post('http://127.0.0.1:20206/json_rpc', json=payload, headers ={'Connection':'close'})

#read response
if (r. status_code == requests.codes.ok):
    jsondata = r.json()
    result = jsondata ["result"]

#result = {
# ’height’:416543
#}
````
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example Phyton script*

# 3.2.1 getblockcount
The method "getblockcount" returns the height of the (currently synced) chain. This is also the
currenty unstable height. This method is called without parameters.

| Result    | Type  | Description             |
| ----------|:-----:| ----------------------- |
|"count" | uint64 | The current blockheight |
|"status"| Strin | Always returns"OK"   |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of getblockcount*

```python
payload = {'jsonrpc':'2.0','id':'1','method':'getblockcount'}
result ={
'count`: 384982,
'status':'OK'
}
````

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of getblockcount output*

# 3.2.2 get_info
The method "get_info" returns various info about the daemon and the state of the network. This
method has no parameters.

| Result    | Type  | Description             |
| ----------|:-----:| ----------------------- |
|"alt_blocks_count" | uint64 | Unused |
|"difficulty" | uint64 | The current difficulty |
|"grey_peerlist_size" | uint64 | Unused |
|"height"| int64 | Current blockchain height |
|"stableheight" | int64 | Current stable height |
|"topoheight" | int64 | Current topoheight |
|"averageblocktime50" | float32 | Average blocktime of the last 50 blocks |
|"incoming_connections_count" | uint64 | Unused |
|"outgoing_connections_count" | uint64 | Unused |
|"target" | uint64 | | Target blocktime in seconds |
|"target_height" | uint64 | | Unused |
|"testnet"| bool | Indicates if this is a testnet |
|"top_block_hash"| string | Block ID of the newest block |
|"tx_count"| uint64 | | Unused |
|"tx_pool_size"| uint64 | Number of pending transactions in the mempool |
|"dynamic_fee_per_kb"| uint64 | Transaction fee |
|"total_supply"| uint64 | Total coin supply (minus premine) |
|"median_block_Size"| uint64 | Max blocksize in bytes (currently 1.25 MB) |
|"white_peerlist_size"| uint64 | Unused |
|"version"| string | Daemon version |
|"status"| string | Always returns"OK"|

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of get_info*

````python
payload = {'jsonrpc':'2.0','id':'1','method':'get_info'}

result = {
'alt_blocks_count': 0,
'difficulty': 2053657306,
'grey_peerlist_size': 0,
'height': 406525,
'stableheight': 406510,
'topoheight': 579299,
'averageblocktime50': 6,
'incoming_connections_count': 0,
'outgoing_connections_count': 0,
'target': 12,
'target_height': 0,
'testnet': False,
'top_block_hash':'4db40b72dba3b179dd10ecf7e90d55934509ee17c3b6de57bca5fefa3237315e',
'tx_count': 0,
'tx_pool_size': 0,
'dynamic_fee_per_kb': 1000000000,
'total_supply': 3393288,
'median_block_size': 1310720,
'white_peerlist_size': 0,
'version':'2.0.1 -3.alpha.atlantis+04072018',
'status':'OK'
}
````

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of get_info output*

# 3.2.3 getblocktemplate
Return a block template (used for mining a block).

| Parameter | Type  | Description             |
| ----------|:-----:| ----------------------- |
|"wallet_address"| string | Hexdecimal string of the wallet address which receives the mining reward |
|"reserve_size"| uint64 | should be > 0 and < 255 |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Parameters for getblocktemplate*

| Result | Type  | Description             |
| ----------|:-----:| -------------------- |
|"blocktemplate_blob"| string | Hexdecimal string of the blocktemplate data |
|"blockhashing_blob"| string | Returns the getwork style blob, ready for either submitting the block or doing Pow Calculations |
|"expected_reward"| uint64 | Always returns 0, not implemented yet |
|"difficulty"| uint64 | The difficulty of the block |
|"height"| uint64 | The height of the block |
|"prev_hash"| string | The hash of the previous block |
|"reserved_offset"| uint64 | Returns the byte position of the extra nonce in the blockhashing blob |
|"epoch"| uint64 | The expiry time of this block |
|"status"| string | Always returns"OK"|

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of getblocktemplate*

````python
payload = {'jsonrpc':'2.0','id':'1','method':'getblocktemplate',"params":{
"wallet_address":"dERokSea2psYGJ ...","reserve_size":10}}
result = {
'blocktemplate_blob':'02028 ed7b2db05cb99daea00000000000000000...',
'blockhashing_blob':'02028 eab6c5b00fe0311b61b2fd324cfb7b01f...',
'expected_reward': 0,
'difficulty': 1804159513,
'height': 392836,
'prev_hash':'a7e861a0a3362e9eb713f4cc1f3da04952914636107266ee5dbbfe ...',
'reserved_offset':43,
'epoch': 1533848474,
'status':'OK'
}
````
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of getblocktemplate output*

# 3.2.4 submitblock
Submits a processed blocktemplate_blob and blockhashing_blob to the daemon. The parameter
is unnamed as the data is transmitted as array and accessed by-position
(see https://www.jsonrpc.org/specification#parameter_structures).

| Parameter | Type  | Description             |
| ----------|:-----:| ----------------------- |
| Parameter Type Description | [ ]string | Array (without name) containing the processed
blocktemplate_blob and blockhashing_blob in hex |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Parameters for submitblock*

| Result | Type  | Description             |
| ----------|:-----:| -------------------- |
|"blid"| string | The new Block ID |
|"status"| string | Returns "OK" if ok, otherwise an error message
e.g."Could NOT decode block", "REJECTED" etc. |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of submitblock*

````python
payload = {'jsonrpc':'2.0','id':'1','method':'submitblock',"params":blockDatainHEX}
Answer : {
'blid': 591042,
'status':'OK'
}
````

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of submitblock output*

# 3.2.5 getlastblockheader
The method "getlastblockheader" returns the latest blockheader of the (currently synced) chain.
This is equal to the top unstable height. This method is called without parameters.

| Result | Type  | Description             |
| ----------|:-----:| -------------------- |
| "block_header" | block_header | The block header |
| "status" | string | Always returns "OK" |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of getlastblockheader*

| Key | Type  | Description             |
| ----------|:-----:| ----------------- |
|"depth"| int64 | The difference between the current blockchain height and the height of this block |
|"difficulty"| string | Difficulty of this block |
|"hash"| string | Hash of the block, serves as block ID |
|"height"| int64 | The height of the block |
|"topoheight"| int64 | The topheight of the block |
|"major_version"| uint64 | Current Atlanis blocks have major version "2"|
|"minor_version"| uint64 | Current Atlanis blocks have minor version "2"|
|"nonce"| string | The block nonce |
|"orphan_status"| bool | Indicates if a block is orphaned, should not happen with Atlantis |
|"syncblock"| bool | Indicates wether a block is a syncblock, that is a single stable block used for rebuilding the chain |
|"txcount"| int64 | Number of transactions included in the block |
|"reward"| uint64 | The reward (base + fees) for this block |
|"tips"| []string | Block IDs of the parent of this block |
|"timestamp"| uint64 | The timestamp of the block |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*JSON structure block_header*

````python
payload = {'jsonrpc':'2.0','id':'1','method':'getlastblockheader'}

result = {
'block_header':
{
'depth': 0,
'difficulty':'2049682764',
'hash':'5 d49e6e9eea00a7c066e14f4ebc05473b39306d8ba05d741f3955658f17322e2',
'height': 397287 ,
'topoheight': 563285 ,
'major_version': 2,
'minor_version': 2,
'nonce': 806404222,
'orphan_status': False,
'syncblock': False,
'txcount': 0,
'reward': 1496206893845,
'tips': ['7527285409f6b7133153a25a1f2f9848dc95758a0be7e9d79365ac3854841644','e9f065645839501f43ce1aae95e491d19ae542fabd99a33b049793862720647c'],'timestamp': 1533702138
},
'status':'OK'
}
````
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of getlastblockheader output*

# 3.2.6 getblockheaderbyhash
The method "getblockheaderbyhash" returns the blockheader for the supplied blocks hash.

| Parameter | Type  | Description             |
| ----------|:-----:| ----------------------- |
|"hash"| string | The hash (block ID) |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Parameters for getblockheaderbyhash*

| Result | Type  | Description             |
| ----------|:-----:| -------------------- |
|"block_header"| block_header | The block header, description of this structure can be found in 3.2.5 |
|"status"| string | Always returns"OK"|

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of getblockheaderbyhash*

````python
payload = {'jsonrpc':'2.0','id':'1','method':'getblockheaderbyhash',"params": {"hash":'7 b6113e05eb72f7ed4231079f97f2708 ...'}}

result =
{'block_header':
{
'depth': 112634 ,
'difficulty':'1938163580',
'hash':'7 b6113e05eb72f7ed4231079f97f2708c6c0eff8cb8a0eb2c079b7ebcdd90157',
'height': 320166 ,
'topoheight': 432401 ,
'major_version': 2,
'minor_version': 2,
'nonce': 2754379831 ,
'orphan_status': False ,
'syncblock': True ,
'txcount': 0,
'reward': 1515705893956 ,
'tips': ['59 a67a563e768da4e8d30940485c37fa22beea1da80c8850da6e690a2467ae5a'],
'timestamp': 1532790081
},
'status':'OK'
}
````

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of getblockheaderbyhash output*

# 3.2.7 getblockheaderbytopoheight
The method "getblockheaderbytopoheight" returns the blockheader for the supplied topoheight.

| Parameter | Type  | Description             |
| ----------|:-----:| ----------------------- |
|"topheight"| uint64 | The topoheight |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Parameters for getblockheaderbytopoheight*

| Result | Type  | Description             |
| ----------|:-----:| -------------------- |
|"block_header"| block_header | he block header, description of this structure can be found in 3.2.5 |
|"status"| string | Always returns"OK"|

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of getblockheaderbytopoheight*


````python
payload = {'jsonrpc':'2.0','id':'1','method':'getblockheaderbytopoheight',"params":{"topoheight":320000}}

result = {
'block_header':
{
 'depth': 185434 ,
 'difficulty':'1967934625',
 'hash':'d4fb3bbba2e6c0260330169f0b7f947c8c470b10a4e2f37d27d3047fd74d4bea',
 'height': 247366 ,
 'topoheight': 320000 ,
 'major_version': 2,
 'minor_version': 2,
 'nonce': 3346301122 ,
 'orphan_status': False ,
 'syncblock': False ,
 'txcount': 0,
 'reward': 1027132841775 ,
 'basereward': 1027132841775 ,
 'tips': ['2cc6b73cc75b81accb9867befb72fff1b4031a44792607f21a9d9ed049baab92','
     eb2258c6459e05966d88bcc6b46191910a512ffa17f7f813c480fe0682456f38'],
'timestamp': 1531920078
},
'status':'OK'
}
````
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of getblockheaderbytopoheight output*

# 3.2.8 getblockheaderbyheight
The method "getblockheaderbyheight" returns the blockheader for the supplied blockchain topoheight,
it does the same as the getblockheaderbytopoheight function.

| Parameter | Type  | Description             |
| ----------|:-----:| ----------------------- |
|"height"| uint64 | The blockchain height |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Parameters for getblockheaderbyheight*

| Result | Type  | Description             |
| ----------|:-----:| -------------------- |
|"block_header"| block_header | The block header, description of this structure can be found in 3.2.5 |
|"status"| string | Always returns"OK"|

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of getblockheaderbyheight*

````python
payload = {'jsonrpc':'2.0','id':'1','method':'getblockheaderbyheight',"
params":{"height":320000}}
result = {
'block_header':
{
'depth': 185434 ,
'difficulty':'1967934625',
'hash':'d4fb3bbba2e6c0260330169f0b7f947c8c470b10a4e2f37d27d3047fd74d4bea',
'height': 247366 ,
'topoheight': 320000 ,
'major_version': 2,
'minor_version': 2,
'nonce': 3346301122 ,
'orphan_status': False ,
'syncblock': False ,
'txcount': 0,
'reward': 1027132841775 ,
'basereward': 1027132841775 ,
'tips': ['2 cc6b73cc75b81accb9867befb72fff1b4031a44792607f21a9d9ed049baab92','
eb2258c6459e05966d88bcc6b46191910a512ffa17f7f813c480fe0682456f38'],
'timestamp': 1531920078
},
'status':'OK'
}
````
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of getblockheaderbyheight output*

# 3.2.9 getblock
The method "getblock" returns the data of a block from either the given height or hash.

| Parameter | Type  | Description             |
| ----------|:-----:| ----------------------- |
| "hash" | string | Hash (block ID) of the block |
| "height" | uint64 | height of the block |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Parameters for getblock*

| Result | Type  | Description             |
| ----------|:-----:| -------------------- |
| "blob" | string | Hexdecimal blob of the block data |
| "json" | string | String with the block data in JSON format |
| "block_header" | block_header | The block header, description of this structure can be found in 3.2.5 |
| "status" | string | Always returns "OK" |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of getblock*

```python
payload = {'jsonrpc': '2.0', 'id':'1', 'method': 'getblock', "params":{ "hash":"ded835887cea53195ca4e1d294d5158c ... "}}

result = {
'blob': '0202 dbc5aedb059080245b6b6a71c24e06d48b00 ... ',
'json':
{
  "major_version ":2,
  "minor_version ":2,
  "timestamp" :1533780699,
  "nonce" :1529118864,
  "miner_tx":
  {
  "version":2,
  "unlock_time" :404016,
  "Vin" :[{ " Height " :403956}],
  "Vout":[
  {
  "Amount":0,
  "Target":{" Key ":" 94507 a4d702b85f601ea51a97 ... "}}],
  "Extra":" AYyPD2XX6QEB19Xx9J0V3 + UpXxZHEcQ2rGENQVHR2738 ",
  "RctSignature ":
  {
  "Message":" 00000000000000... ",
  "MixRing":null ,
  "ECdhInfo":null ,
  "OutPk":null ,
  "Txid":" 000000000000000000... ",
  "BulletSigs":null ,
  "MlsagSigs": null
  }
  },
  "tips":[" d7fc7c9d060e26bd9ca222 ... "],
  "tx_hashes": null
}',
'block_header': see getlastblockheader

}
````
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of getblockheaderbyheight output*

# 3.2.10 gettxpool
The method "gettxpool" returns the tx hashes that are currently in the mempool. This method
has no parameters.

| Result | Type  | Description             |
| ----------|:-----:| -------------------- |
| "tx" | [ ]string | Tx hashes that are in the mempool |
| "status" | string | Always returns "OK" |

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Results of gettxpool*

```python
payload = {'jsonrpc': '2.0', 'id':'1', 'method': 'gettxpool'}

#(If txpool empty)
Result = {
'status ': 'OK'
}

#else
Result = {
'txs ': ['d1a63adf3385f44a20f451a9c38a3b3f6ce0071876b32a3ff7de12b92ccba6c2', '0c237ebf3daaab36acde2cfbbad31e5d5435a114d691abeaf2b407d3c03560ac', 'e5b3e7f49b911734196835fe9a0718fab5f17432aa69c55a035cdee2a1765a7d'],
'status': 'OK'
}
````
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example of gettxpool output*




