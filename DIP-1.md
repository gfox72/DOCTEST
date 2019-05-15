**AUTHOR:** DCAB, Dank

**STATUS:** Active

**Created** 2019-05-14


# DIP-1: DIP Purpose and Guidelines 

## Table of contents
1. [What is a DIP ?](#WhatisaDIP)
2. [Dip Rationale](#DipRationale)
3. [Dip Editors](#DipEditors)
4. [Dip Types](#DipTypes)
5. [Dip Formats and templates](#DipFormats)
6. [Dip Workflow](#DipWorkflow)




## What is a DIP ? <a name="WhatisaDIP"></a>
DIP stands for Dero Improvement Proposal. A DIP is a design document providing information to the Dero community, describing a new feature or its processes or environment. The DIP provides a concise technical specification of the feature and a rationale for the feature. The DIP author is responsible for building consensus within the community and documenting dissenting opinions.

## DIP Rationale <a name="DIPRationale"></a>
We intend DIPs to be the primary instrument for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have in result gone into Dero. DIPs are maintained as documents with a revision control. For DERO implementers, DIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the DIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

## DIP Editors <a name="DIPEditors"></a>
The current DIP editors are (discord handles):

  * `Dank - Dank#8384` <br/>
  * `Captain - Captain#0795` <br/>

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
  *	A **Standard Track DIP** describes any change that affects most or all DERO implementations, such as a change to the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using DERO. Furthermore Standard DIPs can be broken down into the following categories. Standards Track DIPs consist of three parts, a design document, implementation, and finally if warranted an update to the formal specification.
    * **Core** - improvements requiring a consensus fork as well as changes that are not necessarily consensus critical but may be relevant to core dev discussions such as miner/node strategy changes.
    * **Networking** – core dev to comment
    *	**Interface** - includes improvements around client API/RPC specifications and standards and also certain language-level standards. The label “interface” aligns with the interface repository and discussion should primarily occur in that repository before a DIP is submitted to the DIPs repository.
    *	**ERC** - application-level standards and conventions, including contract standards such as token standards, name registries, URI schemes, library/package formats and wallet formats.
  *	A **Meta DIP** describes a process surrounding Ethereum or proposes a change to (or an event in) a process. Process DIPs are like Standards Track DIPs but apply to areas other than the DERO protocol itself. They may propose an implementation, but not to DERO’s codebase; they often require community consensus; unlike Informational DIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in DERO development. Any meta-DIP is also considered a Process DIP.
  *	An **Informational DIP** describes a DERO design issue, or provides general guidelines or information to the DERO community, but does not propose a new feature. Informational DIPs do not necessarily represent DERO community consensus or a recommendation, so users and implementers are free to ignore Informational DIPs or follow their advice.

It is highly recommended that a single DIP contain a single key proposal or new idea. The more focused the DIP, the more successful it tends to be. A change to one client doesn’t require an DIP; a change that affects multiple clients, or defines a standard for multiple apps to use, does.

A DIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.

## DIP Formats and Templates <a name="DIPFormats"></a>
DIPs should be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) style. Image files should be included in a subdirectory of the `assets` folder for that DIP as follows: `assets/dip-X` (for dip X). When linking to an image in the DIP, use relative links such as `../assets/dip-X/image.png`.

## DIP Workflow <a name="DIPWorkflow"></a>
Parties involved in the process are you, the champion or DIP author, the DIP editors, and the DERO Core Developpers

**:warning:** Before you begin, vet your idea, this will save you time. Ask the DERO community first if an idea is original to avoid wasting time on something that will be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where DERO is used. Examples of appropriate public forums to gauge interest around your DIP include DERO discord (general channel), the DERO Community Advisory Board members or DERO telegram.

Your role as the champion is to write the DIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful DIP will move along:

`[WIP] -> [DRAFT] -> [LAST CALL] -> [ACCEPTED] -> [FINAL]`

Each status change is requested by the DIP author and reviewed by the DIP editors. Please include a link to where people should continue discussing your DIP. The DIP editors will process these requests as per the conditions below.
  * **Active** – Some Informational and Process DIPs may also have a status of “Active” if they are never meant to be completed. 
  * **Work in progress** (WIP) – Once the champion has asked the community whether an idea has any chance of support, they will write a draft DIP as a pull request **<<NEEDS LINK**. Consider including an implementation if this will aid people in studying the DIP.
    * :arrow_right: Draft – If agreeable, DIP editor will assign the DIP a number (generally the issue or PR number related to the DIP). The DIP editor will not unreasonably deny an DIP.
    * :x: Draft – Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not in keeping with the DERO philosophy **<<NEEDS CREATION&LINK**.
  * **Draft** – Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the DIP to be mature and ready to proceed to the next status. An DIP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core DIPs).
    * :arrow_right: Last Call – If agreeable, the DIP editor will assign Last Call status and set a review end date `(review-period-end)`, normally 14 days later.
    * :x: Last Call – A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that DIPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed.
  * **Last Call** – This DIP will listed prominently on the website **<<NEEDS LINKK** (subscribe via RSS at last-call.xml **<<NEEDS LINKK**).
    * :x: A Last Call which results in material changes or substantial unaddressed technical complaints will cause the DIP to revert to Draft.
    * :arrow_right: Accepted (Core DIPs only) – A successful Last Call without material changes or unaddressed technical complaints will become Accepted.
    * :arrow_right: Final (Not core DIPs) – A successful Last Call without material changes or unaddressed technical complaints will become Final.
  * **Accepted (Core DIPs only)** – This DIP is in the hands of the Ethereum client developers. Their process for deciding whether to encode it into their clients as part of a hard fork is not part of the DIP process.
    * :arrow_right: Final – Standards Track Core DIPs must be implemented in at least three viable Ethereum clients before it can be considered Final. When the implementation is complete and adopted by the community, the status will be changed to “Final”.
  * **Final** – This DIP represents the current state-of-the-art. A Final DIP should only be updated to correct errata.
  
Other exceptional statuses include:

  * **Deferred** – This is for core DIPs that have been put off for a future hard fork.
  * **Rejected** – An DIP that is fundamentally broken or a Core DIP that was rejected by the Core Devs and will not be implemented.
  * **Active** – This is similar to Final, but denotes an DIP which may be updated without changing its DIP number.
  * **Superseded** – An DIP which was previously final but is no longer considered state-of-the-art. Another DIP will be in Final status and reference the Superseded DIP.
