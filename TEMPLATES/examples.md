---
category: NA
ref: 0
title: MARKDOWN EXAMPLES
author: Gfox
created: 2019/05/17
status: ACTIVE
---

This is *italic* and **bold** 

# Header 1
## Header 2
### Header 3

  * Bullet1 is done by double space and *
    * Bullet 2 is done by 4x space and *
      * you get the point, in markdown editor this is highlighted red, not sure why at this point
        * and so on
        
        
## Links
This is a [link](#test) to a section further down which has a html tag referenced here with a #.


## Images
Html language is used to size and position images
<img align="right" src="/ASSETS/DERO_LOGO_320x320.png" width="80">

## Line breaks
This
is
an example without breaks

This
</br>
is
</br>
an example


## Table of contents
Below uses bullets/indents and links to the ones further down the document.

  * 1 [Chapter 1](#test)
    * 1.1 [Section 1](#1.1)
    * 1.2 [Section 2](#1.1)
  * 2 [Chapter 2](#1.1)
  * 3 [Chapter 3](#test)
    * 3.1 [Section 1](#1.1)
    * 3.2 [Section 2](#test)
    
    
## Code blocks
Code blocks can be simple
```
curl -X POST http://127.0.0.1:20206/json_rpc -d'{"jsonrpc":"2.0","id":"1","method":"getblockcount"}'-H'Content-Type: application / json'
```
or they can use colored syntax if the language is provided
```python
if (i == 1) then {
  i = 1;
}
````

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;*Example in Curl*

<a name="test"></a>
The links will land here

<a name="1.1"></a>
or here



