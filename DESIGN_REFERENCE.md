---
type: INFO
ref: 1
title: DERO DOCUMENT DESIGN REFERENCE
author: Gfox
created: 2019/05/14
---

<img align="right" src="/ASSETS/DERO_LOGO_320x320.png" width="80">
</br>
</br>

# INF0-1: DERO DOCUMENT DESIGN REFERENCE

## Table of contents
1. [Why content management system ?](#whyCMS)
2. [What is this document about ?](#about)
3. [Who does what ?](#whoDoesWhat)
4. [Document types](#docTypes)
5. [Documentation workflow](#docWorkflow)
6. [Design guidelines](#docDesign)

## Why content management system ?<a name="whyCMS"></a>
As projects evolve and grow, it is important to maintain structure and formatting in its documentation, allowing for decentralized contribution.
Since most project information is gathered on Github, the Dero core team has chosen to maintain its documentation under a dedicated Github repository,
adapt to the markdown format and apply similar principles implemented by other reference projects such as Bitcoin or Etherium.

## What is this document about ?<a name="about"></a>
This document provides guidelines to the process of documentation creation. It covers which type of documents will be used in the Dero project
and will also with some examples, provide guidance how these documents should be created and formatted. It is expected that once the basic documentation 
is established, the community will use this document to support further creation and editing.

## Who does what ? <a name="about"></a>
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

## Document types <a name="docTypes"></a>
As the project grows, decisions on different document types may evolve in function of the demand from its community and individuals 
developping on the Dero blockchain. Currently, the following types/categories are considered required to start with:
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

## Design guidelines <a name="docWorkflow"></a>
Following design guidelines apply to all types of documentation and are to be applied by document authors:

Each document should be written in markdown format and start with a header as descrived also in DIB-1 which will provide a table structure 
at top of the document:
> `---` </br>
> `type:`</br>
> `ref:`</br>
> `title:`</br>
> `author:`</br>
> `created:`</br>
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

The the first reference/chapter with the link used for the table of contents or reference within the document:
> `## Chapter 1 <a name="link1"></a>`

For formatting you can reference the [general markdown syntax for github](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) but hereafter some quick examples of the most commonly used ones:

`**bold text**`gives **bold text**
` * first bullet`gives a bullet like below
  * first bullet
`    * second bullet`givess a secondary bullet like below
    * second bullet
    
This document itself can also be reviewed for most common MD syntax.










