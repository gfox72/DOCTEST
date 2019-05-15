

<h2><a id="user-content-what-is-an-edgip" class="anchor" aria-hidden="true" href="#what-is-an-efdfip"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>What is an EIP?</h2>
<p>EIP stands for Ethereum Improvement Proposal. An EIP is a design document providing information to the Ethereum community, or describing a new feature for Ethereum or its processes or environment. The EIP should provide a concise technical specification of the feature and a rationale for the feature. The EIP author is responsible for building consensus within the community and documenting dissenting opinions.</p>
<h2><a id="user-content-eip-rationale" class="anchor" aria-hidden="true" href="#eip-rationale"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>EIP Rationale</h2>
<p>We intend EIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into Ethereum. Because the EIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.</p>
<p>For Ethereum implementers, EIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the EIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.</p>
<h2><a id="user-content-eip-types" class="anchor" aria-hidden="true" href="#eip-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>EIP Types</h2>
<p>There are three types of EIP:</p>
<ul>
<li>A <strong>Standard Track EIP</strong> describes any change that affects most or all Ethereum implementations, such as a change to the network protocol, a change in block or transaction validity rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using Ethereum. Furthermore Standard EIPs can be broken down into the following categories. Standards Track EIPs consist of three parts, a design document, implementation, and finally if warranted an update to the <a href="https://github.com/ethereum/yellowpaper">formal specification</a>.
<ul>
<li><strong>Core</strong> - improvements requiring a consensus fork (e.g. <a href="https://github.com/ethereum/EIPs/blob/master/EIPS/eip-5.md">EIP5</a>, <a href="https://github.com/ethereum/EIPs/issues/28">EIP101</a>), as well as changes that are not necessarily consensus critical but may be relevant to <a href="https://github.com/ethereum/pm">“core dev” discussions</a> (for example, <a href="https://github.com/ethereum/EIPs/issues/90">EIP90</a>, and the miner/node strategy changes 2, 3, and 4 of <a href="https://github.com/ethereum/EIPs/issues/86#issue-145324865">EIP86</a>).</li>
<li><strong>Networking</strong> - includes improvements around <a href="https://github.com/ethereum/wiki/wiki/%C3%90%CE%9EVp2p-Wire-Protocol">devp2p</a> (<a href="https://github.com/ethereum/EIPs/blob/master/EIPS/eip-8.md">EIP8</a>) and <a href="https://github.com/ethereum/wiki/wiki/Light-client-protocol">Light Ethereum Subprotocol</a>, as well as proposed improvements to network protocol specifications of <a href="https://github.com/ethereum/go-ethereum/wiki/Whisper-Overview">whisper</a> and <a href="https://github.com/ethereum/go-ethereum/pull/2959">swarm</a>.</li>
<li><strong>Interface</strong> - includes improvements around client <a href="https://github.com/ethereum/wiki/wiki/JSON-RPC">API/RPC</a> specifications and standards, and also certain language-level standards like method names (<a href="https://github.com/ethereum/EIPs/blob/master/EIPS/eip-6.md">EIP6</a>) and <a href="https://github.com/ethereum/wiki/wiki/Ethereum-Contract-ABI">contract ABIs</a>. The label “interface” aligns with the <a href="https://github.com/ethereum/interfaces">interfaces repo</a> and discussion should primarily occur in that repository before an EIP is submitted to the EIPs repository.</li>
<li><strong>ERC</strong> - application-level standards and conventions, including contract standards such as token standards (<a href="https://github.com/ethereum/EIPs/issues/20">ERC20</a>), name registries (<a href="https://github.com/ethereum/EIPs/issues/26">ERC26</a>, <a href="https://github.com/ethereum/EIPs/issues/137">ERC137</a>), URI schemes (<a href="https://github.com/ethereum/EIPs/issues/67">ERC67</a>), library/package formats (<a href="https://github.com/ethereum/EIPs/issues/82">EIP82</a>), and wallet formats (<a href="https://github.com/ethereum/EIPs/issues/75">EIP75</a>, <a href="https://github.com/ethereum/EIPs/issues/85">EIP85</a>).</li>
</ul>
</li>
<li>A <strong>Meta EIP</strong> describes a process surrounding Ethereum or proposes a change to (or an event in) a process. Process EIPs are like Standards Track EIPs but apply to areas other than the Ethereum protocol itself. They may propose an implementation, but not to Ethereum's codebase; they often require community consensus; unlike Informational EIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in Ethereum development. Any meta-EIP is also considered a Process EIP.</li>
<li>An <strong>Informational EIP</strong> describes an Ethereum design issue, or provides general guidelines or information to the Ethereum community, but does not propose a new feature. Informational EIPs do not necessarily represent Ethereum community consensus or a recommendation, so users and implementers are free to ignore Informational EIPs or follow their advice.</li>
</ul>
<p>It is highly recommended that a single EIP contain a single key proposal or new idea. The more focused the EIP, the more successful it tends to be. A change to one client doesn't require an EIP; a change that affects multiple clients, or defines a standard for multiple apps to use, does.</p>
<p>An EIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.</p>
<h2><a id="user-content-eip-work-flow" class="anchor" aria-hidden="true" href="#eip-work-flow"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>EIP Work Flow</h2>
<p>Parties involved in the process are you, the champion or <em>EIP author</em>, the <a href="#eip-editors"><em>EIP editors</em></a>, and the <a href="https://github.com/ethereum/pm"><em>Ethereum Core Developers</em></a>.</p>
<p><g-emoji class="g-emoji" alias="warning" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/26a0.png">⚠️</g-emoji> Before you begin, vet your idea, this will save you time. Ask the Ethereum community first if an idea is original to avoid wasting time on something that will be rejected based on prior research (searching the Internet does not always do the trick). It also helps to make sure the idea is applicable to the entire community and not just the author. Just because an idea sounds good to the author does not mean it will work for most people in most areas where Ethereum is used. Examples of appropriate public forums to gauge interest around your EIP include <a href="https://www.reddit.com/r/ethereum/" rel="nofollow">the Ethereum subreddit</a>, <a href="https://github.com/ethereum/EIPs/issues">the Issues section of this repository</a>, and <a href="https://gitter.im/ethereum/" rel="nofollow">one of the Ethereum Gitter chat rooms</a>. In particular, <a href="https://github.com/ethereum/EIPs/issues">the Issues section of this repository</a> is an excellent place to discuss your proposal with the community and start creating more formalized language around your EIP.</p>
<p>Your role as the champion is to write the EIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea. Following is the process that a successful EIP will move along:</p>
<pre><code>[ WIP ] -&gt; [ DRAFT ] -&gt; [ LAST CALL ] -&gt; [ ACCEPTED ] -&gt; [ FINAL ]
</code></pre>
<p>Each status change is requested by the EIP author and reviewed by the EIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your EIP. The EIP editors will process these requests as per the conditions below.</p>
<ul>
<li><strong>Active</strong> -- Some Informational and Process EIPs may also have a status of “Active” if they are never meant to be completed. E.g. EIP 1 (this EIP).</li>
<li><strong>Work in progress (WIP)</strong> -- Once the champion has asked the Ethereum community whether an idea has any chance of support, they will write a draft EIP as a <a href="https://github.com/ethereum/EIPs/pulls">pull request</a>. Consider including an implementation if this will aid people in studying the EIP.
<ul>
<li><g-emoji class="g-emoji" alias="arrow_right" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/27a1.png">➡️</g-emoji> Draft -- If agreeable, EIP editor will assign the EIP a number (generally the issue or PR number related to the EIP) and merge your pull request. The EIP editor will not unreasonably deny an EIP.</li>
<li><g-emoji class="g-emoji" alias="x" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/274c.png">❌</g-emoji> Draft -- Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility, or not in keeping with the <a href="https://github.com/ethereum/wiki/wiki/White-Paper#philosophy">Ethereum philosophy</a>.</li>
</ul>
</li>
<li><strong>Draft</strong> -- Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the EIP to be mature and ready to proceed to the next status. An EIP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core EIPs).
<ul>
<li><g-emoji class="g-emoji" alias="arrow_right" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/27a1.png">➡️</g-emoji> Last Call -- If agreeable, the EIP editor will assign Last Call status and set a review end date (<code>review-period-end</code>), normally 14 days later.</li>
<li><g-emoji class="g-emoji" alias="x" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/274c.png">❌</g-emoji> Last Call -- A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that EIPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed.</li>
</ul>
</li>
<li><strong>Last Call</strong> -- This EIP will listed prominently on the <a href="https://eips.ethereum.org/" rel="nofollow">https://eips.ethereum.org/</a> website (subscribe via RSS at <a href="/ethereum/EIPs/blob/master/last-call.xml">last-call.xml</a>).
<ul>
<li><g-emoji class="g-emoji" alias="x" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/274c.png">❌</g-emoji> -- A Last Call which results in material changes or substantial unaddressed technical complaints will cause the EIP to revert to Draft.</li>
<li><g-emoji class="g-emoji" alias="arrow_right" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/27a1.png">➡️</g-emoji> Accepted (Core EIPs only) -- A successful Last Call without material changes or unaddressed technical complaints will become Accepted.</li>
<li><g-emoji class="g-emoji" alias="arrow_right" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/27a1.png">➡️</g-emoji> Final (Not core EIPs) -- A successful Last Call without material changes or unaddressed technical complaints will become Final.</li>
</ul>
</li>
<li><strong>Accepted (Core EIPs only)</strong> -- This EIP is in the hands of the Ethereum client developers.  Their process for deciding whether to encode it into their clients as part of a hard fork is not part of the EIP process.
<ul>
<li><g-emoji class="g-emoji" alias="arrow_right" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/27a1.png">➡️</g-emoji> Final -- Standards Track Core EIPs must be implemented in at least three viable Ethereum clients before it can be considered Final. When the implementation is complete and adopted by the community, the status will be changed to “Final”.</li>
</ul>
</li>
<li><strong>Final</strong> -- This EIP represents the current state-of-the-art. A Final EIP should only be updated to correct errata.</li>
</ul>
<p>Other exceptional statuses include:</p>
<ul>
<li><strong>Deferred</strong> -- This is for core EIPs that have been put off for a future hard fork.</li>
<li><strong>Rejected</strong> -- An EIP that is fundamentally broken or a Core EIP that was rejected by the Core Devs and will not be implemented.</li>
<li><strong>Active</strong> -- This is similar to Final, but denotes an EIP which may be updated without changing its EIP number.</li>
<li><strong>Superseded</strong> -- An EIP which was previously final but is no longer considered state-of-the-art. Another EIP will be in Final status and reference the Superseded EIP.</li>
</ul>
<h2><a id="user-content-what-belongs-in-a-successful-eip" class="anchor" aria-hidden="true" href="#what-belongs-in-a-successful-eip"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>What belongs in a successful EIP?</h2>
<p>Each EIP should have the following parts:</p>
<ul>
<li>Preamble - RFC 822 style headers containing metadata about the EIP, including the EIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See <a href="https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1.md#eip-header-preamble">below</a> for details.</li>
<li>Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the EIP.</li>
<li>Abstract - a short (~200 word) description of the technical issue being addressed.</li>
<li>Motivation (*optional) - The motivation is critical for EIPs that want to change the Ethereum protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the EIP solves. EIP submissions without sufficient motivation may be rejected outright.</li>
<li>Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current Ethereum platforms (cpp-ethereum, go-ethereum, parity, ethereumJ, ethereumjs-lib, <a href="https://github.com/ethereum/wiki/wiki/Clients">and others</a>.</li>
<li>Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.</li>
<li>Backwards Compatibility - All EIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The EIP must explain how the author proposes to deal with these incompatibilities. EIP submissions without a sufficient backwards compatibility treatise may be rejected outright.</li>
<li>Test Cases - Test cases for an implementation are mandatory for EIPs that are affecting consensus changes. Other EIPs can choose to include links to test cases if applicable.</li>
<li>Implementations - The implementations must be completed before any EIP is given status “Final”, but it need not be completed before the EIP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.</li>
<li>Copyright Waiver - All EIPs must be in the public domain. See the bottom of this EIP for an example copyright waiver.</li>
</ul>
<h2><a id="user-content-eip-formats-and-templates" class="anchor" aria-hidden="true" href="#eip-formats-and-templates"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>EIP Formats and Templates</h2>
<p>EIPs should be written in <a href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet">markdown</a> format.
Image files should be included in a subdirectory of the <code>assets</code> folder for that EIP as follows: <code>assets/eip-X</code> (for eip <strong>X</strong>). When linking to an image in the EIP, use relative links such as <code>../assets/eip-X/image.png</code>.</p>
<h2><a id="user-content-eip-header-preamble" class="anchor" aria-hidden="true" href="#eip-header-preamble"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>EIP Header Preamble</h2>
<p>Each EIP must begin with an RFC 822 style header preamble, preceded and followed by three hyphens (<code>---</code>). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.</p>
<p><code> eip:</code>  (this is determined by the EIP editor)</p>
<p><code> title:</code> </p>
<p><code> author:</code> &lt;a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.&gt;</p>
<p><code> * discussions-to:</code> &lt;a url pointing to the official discussion thread&gt;</p>
<p><code> status:</code> &lt;Draft | Last Call | Accepted | Final | Active | Deferred | Rejected | Superseded&gt;</p>
<p><code>* review-period-end:</code> </p>
<p><code> type:</code> &lt;Standards Track (Core, Networking, Interface, ERC)  | Informational | Meta&gt;</p>
<p><code> * category:</code> &lt;Core | Networking | Interface | ERC&gt;</p>
<p><code> created:</code> </p>
<p><code> * updated:</code> </p>
<p><code> * requires:</code> &lt;EIP number(s)&gt;</p>
<p><code> * replaces:</code> &lt;EIP number(s)&gt;</p>
<p><code> * superseded-by:</code> &lt;EIP number(s)&gt;</p>
<p><code> * resolution:</code> &lt;a url pointing to the resolution of this EIP&gt;</p>
<p>Headers that permit lists must separate elements with commas.</p>
<p>Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).</p>
<h4><a id="user-content-author-header" class="anchor" aria-hidden="true" href="#author-header"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>author</code> header</h4>
<p>The <code>author</code> header optionally lists the names, email addresses or usernames of the authors/owners of the EIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:</p>
<blockquote>
<p>Random J. User &lt;<a href="mailto:address@dom.ain">address@dom.ain</a>&gt;</p>
</blockquote>
<p>or</p>
<blockquote>
<p>Random J. User (@username)</p>
</blockquote>
<p>if the email address or GitHub username is included, and</p>
<blockquote>
<p>Random J. User</p>
</blockquote>
<p>if the email address is not given.</p>
<h4><a id="user-content-resolution-header" class="anchor" aria-hidden="true" href="#resolution-header"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>resolution</code> header</h4>
<p>The <code>resolution</code> header is required for Standards Track EIPs only. It contains a URL that should point to an email message or other web resource where the pronouncement about the EIP is made.</p>
<h4><a id="user-content-discussions-to-header" class="anchor" aria-hidden="true" href="#discussions-to-header"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>discussions-to</code> header</h4>
<p>While an EIP is a draft, a <code>discussions-to</code> header will indicate the mailing list or URL where the EIP is being discussed. As mentioned above, examples for places to discuss your EIP include <a href="https://gitter.im/ethereum/topics" rel="nofollow">Ethereum topics on Gitter</a>, an issue in this repo or in a fork of this repo, <a href="https://ethereum-magicians.org/" rel="nofollow">Ethereum Magicians</a> (this is suitable for EIPs that may be contentious or have a strong governance aspect), and <a href="https://www.reddit.com/r/ethereum/" rel="nofollow">Reddit r/ethereum</a>.</p>
<p>No <code>discussions-to</code> header is necessary if the EIP is being discussed privately with the author.</p>
<p>As a single exception, <code>discussions-to</code> cannot point to GitHub pull requests.</p>
<h4><a id="user-content-type-header" class="anchor" aria-hidden="true" href="#type-header"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>type</code> header</h4>
<p>The <code>type</code> header specifies the type of EIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, networking, interface, or ERC).</p>
<h4><a id="user-content-category-header" class="anchor" aria-hidden="true" href="#category-header"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>category</code> header</h4>
<p>The <code>category</code> header specifies the EIP's category. This is required for standards-track EIPs only.</p>
<h4><a id="user-content-created-header" class="anchor" aria-hidden="true" href="#created-header"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>created</code> header</h4>
<p>The <code>created</code> header records the date that the EIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.</p>
<h4><a id="user-content-updated-header" class="anchor" aria-hidden="true" href="#updated-header"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>updated</code> header</h4>
<p>The <code>updated</code> header records the date(s) when the EIP was updated with "substantial" changes. This header is only valid for EIPs of Draft and Active status.</p>
<h4><a id="user-content-requires-header" class="anchor" aria-hidden="true" href="#requires-header"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>requires</code> header</h4>
<p>EIPs may have a <code>requires</code> header, indicating the EIP numbers that this EIP depends on.</p>
<h4><a id="user-content-superseded-by-and-replaces-headers" class="anchor" aria-hidden="true" href="#superseded-by-and-replaces-headers"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a><code>superseded-by</code> and <code>replaces</code> headers</h4>
<p>EIPs may also have a <code>superseded-by</code> header indicating that an EIP has been rendered obsolete by a later document; the value is the number of the EIP that replaces the current document. The newer EIP must have a <code>replaces</code> header containing the number of the EIP that it rendered obsolete.</p>
<h2><a id="user-content-auxiliary-files" class="anchor" aria-hidden="true" href="#auxiliary-files"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Auxiliary Files</h2>
<p>EIPs may include auxiliary files such as diagrams. Such files must be named EIP-XXXX-Y.ext, where “XXXX” is the EIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).</p>
<h2><a id="user-content-transferring-eip-ownership" class="anchor" aria-hidden="true" href="#transferring-eip-ownership"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Transferring EIP Ownership</h2>
<p>It occasionally becomes necessary to transfer ownership of EIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred EIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the EIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the EIP. We try to build consensus around an EIP, but if that's not possible, you can always submit a competing EIP.</p>
<p>If you are interested in assuming ownership of an EIP, send a message asking to take over, addressed to both the original author and the EIP editor. If the original author doesn't respond to email in a timely manner, the EIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).</p>
<h2><a id="user-content-eip-editors" class="anchor" aria-hidden="true" href="#eip-editors"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>EIP Editors</h2>
<p>The current EIP editors are</p>
<p><code> * Nick Johnson (@arachnid)</code></p>
<p><code> * Casey Detrio (@cdetrio)</code></p>
<p><code> * Hudson Jameson (@Souptacular)</code></p>
<p><code> * Vitalik Buterin (@vbuterin)</code></p>
<p><code> * Nick Savers (@nicksavers)</code></p>
<p><code> * Martin Becze (@wanderer)</code></p>
<p><code> * Greg Colvin (@gcolvin)</code></p>
<p><code> * Alex Beregszaszi (@axic)</code></p>
<h2><a id="user-content-eip-editor-responsibilities" class="anchor" aria-hidden="true" href="#eip-editor-responsibilities"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>EIP Editor Responsibilities</h2>
<p>For each new EIP that comes in, an editor does the following:</p>
<ul>
<li>Read the EIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.</li>
<li>The title should accurately describe the content.</li>
<li>Check the EIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style</li>
</ul>
<p>If the EIP isn't ready, the editor will send it back to the author for revision, with specific instructions.</p>
<p>Once the EIP is ready for the repository, the EIP editor will:</p>
<ul>
<li>
<p>Assign an EIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this EIP)</p>
</li>
<li>
<p>Merge the corresponding pull request</p>
</li>
<li>
<p>Send a message back to the EIP author with the next step.</p>
</li>
</ul>
<p>Many EIPs are written and maintained by developers with write access to the Ethereum codebase. The EIP editors monitor EIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.</p>
<p>The editors don't pass judgment on EIPs. We merely do the administrative &amp; editorial part.</p>
<h2><a id="user-content-history" class="anchor" aria-hidden="true" href="#history"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>History</h2>
<p>This document was derived heavily from <a href="https://github.com/bitcoin/bips">Bitcoin's BIP-0001</a> written by Amir Taaki which in turn was derived from <a href="https://www.python.org/dev/peps/" rel="nofollow">Python's PEP-0001</a>. In many places text was simply copied and modified. Although the PEP-0001 text was written by Barry Warsaw, Jeremy Hylton, and David Goodger, they are not responsible for its use in the Ethereum Improvement Process, and should not be bothered with technical questions specific to Ethereum or the EIP. Please direct all comments to the EIP editors.</p>
<p>December 7, 2015: EIP 1 has been improved and will be placed as a PR.</p>
<p>February 1, 2016: EIP 1 has added editors, made draft improvements to process, and has merged with Master stream.</p>
<p>March 21, 2018: Minor edits to accommodate the new automatically-generated EIP directory on <a href="https://eips.ethereum.org/" rel="nofollow">eips.ethereum.org</a>.</p>
<p>May 29, 2018: A last call process was added.</p>
<p>Oct 17, 2018: The <code>updated</code> header was introduced.</p>
<p>See <a href="https://github.com/ethereum/EIPs/commits/master/EIPS/eip-1.md">the revision history for further details</a>, which is also available by clicking on the History button in the top right of the EIP.</p>
<h3><a id="user-content-bibliography" class="anchor" aria-hidden="true" href="#bibliography"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Bibliography</h3>
<h2><a id="user-content-copyright" class="anchor" aria-hidden="true" href="#copyright"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Copyright</h2>
<p>Copyright and related rights waived via <a href="https://creativecommons.org/publicdomain/zero/1.0/" rel="nofollow">CC0</a>.</p>
</article>
  </div>

    </div>

  

  <details class="details-reset details-overlay details-overlay-dark">
    <summary data-hotkey="l" aria-label="Jump to line"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast linejump" aria-label="Jump to line">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-jump-to-line-form Box-body d-flex" action="" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
        <input class="form-control flex-auto mr-3 linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
        <button type="submit" class="btn" data-close-dialog>Go</button>
</form>    </details-dialog>
  </details>



  </div>
  <div class="modal-backdrop js-touch-events"></div>
</div>

    </main>
  </div>
  

  </div>

        
<div class="footer container-lg width-full p-responsive" role="contentinfo">
  <div class="position-relative d-flex flex-row-reverse flex-lg-row flex-wrap flex-lg-nowrap flex-justify-center flex-lg-justify-between pt-6 pb-2 mt-6 f6 text-gray border-top border-gray-light ">
    <ul class="list-style-none d-flex flex-wrap col-12 col-lg-5 flex-justify-center flex-lg-justify-between mb-2 mb-lg-0">
      <li class="mr-3 mr-lg-0">&copy; 2019 <span title="0.51796s from unicorn-6d5c7bcccc-pqwbf">GitHub</span>, Inc.</li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to terms, text:terms" href="https://github.com/site/terms">Terms</a></li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to privacy, text:privacy" href="https://github.com/site/privacy">Privacy</a></li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to security, text:security" href="https://github.com/security">Security</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://githubstatus.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a data-ga-click="Footer, go to help, text:help" href="https://help.github.com">Help</a></li>
    </ul>

    <a aria-label="Homepage" title="GitHub" class="footer-octicon d-none d-lg-block mx-lg-4" href="https://github.com">
      <svg height="24" class="octicon octicon-mark-github" viewBox="0 0 16 16" version="1.1" width="24" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
</a>
   <ul class="list-style-none d-flex flex-wrap col-12 col-lg-5 flex-justify-center flex-lg-justify-between mb-2 mb-lg-0">
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to contact, text:contact" href="https://github.com/contact">Contact GitHub</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://github.com/pricing" data-ga-click="Footer, go to Pricing, text:Pricing">Pricing</a></li>
      <li class="mr-3 mr-lg-0"><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li class="mr-3 mr-lg-0"><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://github.blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a data-ga-click="Footer, go to about, text:about" href="https://github.com/about">About</a></li>

    </ul>
  </div>
  <div class="d-flex flex-justify-center pb-6">
    <span class="f6 text-gray-light"></span>
  </div>
</div>



  <div id="ajax-error-message" class="ajax-error-message flash flash-error">
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 0 0 0 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 0 0 .01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <button type="button" class="flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
      <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
    </button>
    You can’t perform that action at this time.
  </div>


    
    <script crossorigin="anonymous" integrity="sha512-mFJGqO63IzrRUe/3CpI2x1TacUM1edYB56po0/mrnmI+7ntIf2oo9LZAMT0bW41GpH9NycR6OW2S9vvouQDHWQ==" type="application/javascript" src="https://github.githubassets.com/assets/frameworks-1d50b418.js"></script>
    
    <script crossorigin="anonymous" async="async" integrity="sha512-z2DrP6xrMBP+9ZM0RzRzKr1UUoPp9Seyh1b0sJovSOMdhiRIrpKIt07Dyjtpb/+b+sEEh1U5X357TYb+6WMnqA==" type="application/javascript" src="https://github.githubassets.com/assets/github-bootstrap-4c64d263.js"></script>
    
    
    
  <div class="js-stale-session-flash stale-session-flash flash flash-warn flash-banner" hidden
    >
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 0 0 0 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 0 0 .01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <span class="signed-in-tab-flash">You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
    <span class="signed-out-tab-flash">You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
  </div>
  <template id="site-details-dialog">
  <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark" open>
    <summary aria-haspopup="dialog" aria-label="Close dialog"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast">
      <button class="Box-btn-octicon m-0 btn-octicon position-absolute right-0 top-0" type="button" aria-label="Close dialog" data-close-dialog>
        <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
      </button>
      <div class="octocat-spinner my-6 js-details-dialog-spinner"></div>
    </details-dialog>
  </details>
</template>

  <div class="Popover js-hovercard-content position-absolute" style="display: none; outline: none;" tabindex="0">
  <div class="Popover-message Popover-message--bottom-left Popover-message--large Box box-shadow-large" style="width:360px;">
  </div>
</div>

  <div aria-live="polite" class="js-global-screen-reader-notice sr-only"></div>

  </body>
</html>

