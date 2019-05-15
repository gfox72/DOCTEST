**AUTHOR:** DCAB, Dank

**STATUS:** Active

**Created** 2019-05-14


# DIP-1: DIP Purpose and Guidelines 

## Table of contents
1. [What is a DIP ?](#WhatisaDIP)
2. [Dip Rationale](#DipRationale)
3. [Dip Editors](#DipEditors)





## What is a DIP ? <a name="WhatisaDIP"></a>
DIP stands for Dero Improvement Proposal. A DIP is a design document providing information to the Dero community, describing a new feature or its processes or environment. The DIP provides a concise technical specification of the feature and a rationale for the feature. The DIP author is responsible for building consensus within the community and documenting dissenting opinions.

## DIP Rationale <a name="DIPRationale"></a>
We intend DIPs to be the primary instrument for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have in result gone into Dero. DIPs are maintained as documents with a revision control. For DERO implementers, DIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the DIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

## DIP Editors <a name="DIPEditors"></a>
The current DIP editors are (discord handles):

Dank - Dank#8384<br/>
Captain - Captain#0795<br/>

## DIP Editor Responsibilities
For each new DIP submitted, an editor does the following:
  * Read the DIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don’t seem likely to get to final status.
  * The title should accurately describe the content.
  * Check the DIP for language (spelling, grammar, sentence structure, etc.), markup, code style.

If the DIP isn’t ready, the editor will send it back to the author for revision with specific instructions.<br/>

Once the DIP is ready for the repository, the DIP editor will:
  *	Assign a DIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this DIP)
  *	Send a message back to the DIP author with the next step.
  
Most of the DIPs are written and maintained by developers with write access to the DERO codebase. The DIP editors monitor DIP changes and correct any structure, grammar, spelling, or markup mistakes they see.
Editors don’t pass judgment on DIPs, they merely do the administrative & editorial part.

## DIP Types <a name="DIPTypes"></a>
There are three types of DIP:
  *	A Standard Track DIP describes any change that affects most or all DERO implementations, such as a change to the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using DERO. Furthermore Standard DIPs can be broken down into the following categories. Standards Track DIPs consist of three parts, a design document, implementation, and finally if warranted an update to the formal specification.
   * Core - improvements requiring a consensus fork as well as changes that are not necessarily consensus critical but may be relevant to core dev discussions such as miner/node strategy changes.
   * Networking – core dev to comment
o	Interface - includes improvements around client API/RPC specifications and standards and also certain language-level standards. The label “interface” aligns with the interface repository and discussion should primarily occur in that repository before a DIP is submitted to the DIPs repository.
o	ERC - application-level standards and conventions, including contract standards such as token standards, name registries, URI schemes, library/package formats and wallet formats.
•	A Meta DIP describes a process surrounding Ethereum or proposes a change to (or an event in) a process. Process DIPs are like Standards Track DIPs but apply to areas other than the DERO protocol itself. They may propose an implementation, but not to DERO’s codebase; they often require community consensus; unlike Informational DIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in DERO development. Any meta-DIP is also considered a Process DIP.
•	An Informational DIP describes a DERO design issue, or provides general guidelines or information to the DERO community, but does not propose a new feature. Informational DIPs do not necessarily represent DERO community consensus or a recommendation, so users and implementers are free to ignore Informational DIPs or follow their advice.
It is highly recommended that a single DIP contain a single key proposal or new idea. The more focused the DIP, the more successful it tends to be. A change to one client doesn’t require an DIP; a change that affects multiple clients, or defines a standard for multiple apps to use, does.
A DIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.

