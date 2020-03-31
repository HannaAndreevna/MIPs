---
mip: 1
title: MIP Purpose and Guidelines
status: Active
type: Meta
author: Yury Glushkov (@PaterSantyago)
created: 2020-03-30
---

## What is a MIP?

MIP stands for MAVN Improvement Proposal. A MIP is a design document providing information to the MAVN community, or describing a new feature for OpenMAVN or its processes or environment. The MIP should provide a concise technical specification of the feature and a rationale for the feature. The MIP author is responsible for building consensus within the community and documenting dissenting opinions.

## MIP Rationale

We intend MIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into MAVN. Because the MIPs are maintained  as text files in a versioned repository, their revision history is the historical record of the feature proposal.

## MIP Types

There are three types of MIP:

- A **Use Case MIP** describes a use-case for OpenMAVN platform or propose a change to the existing one.
- A **Technical MIP** describes any changes, that affect OpenMAVN code base, but do not affect existing use-cases.
- A **Meta MIP** describes a process surrounding OpenMAVN or proposes a change to (or an event in) a process. Process MIPs are like Feature MIPs but apply to areas other than the OpenMAVN itself. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in OpenMAVN development.
- An **Informational MIP** describes an OpenMAVN design issue, or provides general guidelines or information to the MAVN community, but does not propose a new feature.

It is highly recommended that a single MIP contain a single key proposal or new idea. The more focused the MIP, the more successful it tends to be.

A MIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the platform unduly.

## MIP Workflow

### Shepherding a MIP

Parties involved in the process are you, the hero or *MIP author*, the [*MIP editors*](#mip-editors), and the [*Core Team*](#core-team).


Before you begin writing a formal MIP, you should vet your idea. Ask the MAVN community first if an idea is original to avoid wasting time on something that will be be rejected based on prior research. It is thus recommended to open a discussion thread on [the Issues section of this repository] to do this, but you can also use [the OpenMAVN MIPs Telegram group] or the #mips channel in [the OpenMAVN Slack workspace]. 

In addition to making sure your idea is original, it will be your role as the author to make your idea clear to reviewers and interested parties, as well as inviting editors, developers and community to give feedback on the aforementioned channels. You should try and gauge whether the interest in your MIP is commensurate with both the work involved in implementing it and how many parties will have to conform to it. Negative community feedback will be taken into consideration and may prevent your MIP from moving past the Draft stage.

*In short, your role as the hero is to write the EIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea.*

### MIP Process 

Following is the process that a successful MIP will move along:

```
[ IDEA ] -> [ DRAFT ] -> [ LAST CALL ] -> [ ACCEPTED ] -> [ FINAL ]
```

Each status change is requested by the MIP author and reviewed by the MIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your MIP. The MIP editors will process these requests as per the conditions below.

* **Idea** -- Once the hero has asked the MAVN community whether an idea has any chance of support, they will write a draft MIP as a [pull request]. Consider including an implementation if this will aid people in studying the MIP.
  * :arrow_right: Draft -- If agreeable, MIP editor will assign the MIP a number (generally the issue or PR number related to the MIP) and merge your pull request. The MIP editor will not unreasonably deny an MIP.
  * :x: Draft -- Reasons for denying draft status include but are not limited to being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility.
* **Draft** -- Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the MIP to be mature and ready to proceed to the next status.
  * :arrow_right: Last Call -- If agreeable, the MIP editor will assign Last Call status and set a review end date (`review-period-end`), normally 14 days later.
  * :x: Last Call -- A request for Last Call status will be denied if material changes are still expected to be made to the draft. We hope that MIPs only enter Last Call once, so as to avoid unnecessary noise on the RSS feed.
* **Last Call** -- This MIP will listed prominently on the [mips.mavn.ch](https://mips.mavn.ch/) website (subscribe via RSS at [last-call.xml](/last-call.xml)).
  * :x: -- A Last Call which results in material changes or substantial unaddressed technical complaints will cause the MIP to revert to Draft.
  * :arrow_right: Accepted -- A successful Last Call without material changes or unaddressed technical complaints will become Accepted.
* **Accepted** -- This status signals that this MIP is ready for inclusion into backlog.
  * :arrow_right: Draft -- The Core Team can decide to move this MIP back to the Draft status at their discretion. E.g. a major, but correctable, flaw was found in the MIP.
  * :arrow_right: Rejected -- The Core Team can decide to mark this MIP as Rejected at their discretion. E.g. a major, but uncorrectable, flaw was found in the MIP.
  * :arrow_right: Final -- MIPs must be implemented and all necessary changes must be merged into master branch(es) before it can be considered Final. When the implementation is complete, the status will be changed to “Final”.
* **Final** -- This MIP represents the current state-of-the-art. A Final MIP should only be updated to correct errata.

Other exceptional statuses include:

* **Active** -- Some Informational and Meta MIPs may also have a status of “Active” if they are never meant to be completed. E.g. MIP 1 (this MIP).
* **Abandoned** -- This MIP is no longer pursued by the original authors or it may not be a (technically) preferred option anymore.
  * :arrow_right: Draft -- Current authors or new hero wishing to pursue this MIP can ask for changing it to Draft status.
* **Rejected** -- A MIP that is fundamentally broken or rejected by the Core Team and will not be implemented. A MIP cannot move on from this state.
* **Superseded** -- A MIP which was previously Final but is no longer considered state-of-the-art. Another MIP will be in Final status and reference the Superseded MIP. A MIP cannot move on from this state.

## What belongs in a successful MIP?

Each MIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the MIP, including the MIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See [below](https://github.com/OpenVASP/MIPs/blob/master/MIPS/mip-1.md#mip-header-preamble) for details.
- Abstract - A short (~200 word) description of the technical issue being addressed.
- Motivation (*optional) - The motivation is critical for MIPs that want to change the OpenMAVN platform. It should clearly explain why the existing platform implementation is inadequate to address the problem that the MIP solves. MIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other platforms. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Backwards Compatibility - All MIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The MIP must explain how the author proposes to deal with these incompatibilities. MIP submissions without a sufficient backwards compatibility treatise may be rejected outright.
- Test Cases - Test cases for an implementation are mandatory for MIPs that are affecting code base. Other MIPs can choose to include links to test cases if applicable.
- Implementations - The implementations must be completed before any MIP is given status “Final”, but it need not be completed before the MIP is merged as draft. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of “rough consensus and running code” is still useful when it comes to resolving many discussions of API details.
- Security Considerations - All MIPs must contain a section that discusses the security implications/considerations relevant to the proposed change. Include information that might be important for security discussions, surfaces risks and can be used throughout the life cycle of the proposal. E.g. include security-relevant design decisions, concerns, important discussions, implementation-specific guidance and pitfalls, an outline of threats and risks and how they are being addressed. MIP submissions missing the "Security Considerations" section will be rejected. A MIP cannot proceed to status "Final" without a Security Considerations discussion deemed sufficient by the reviewers.
- Copyright Waiver - All MIPs must be in the public domain. See the bottom of this MIP for an example copyright waiver.

## MIP Formats and Templates

MIPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that MIP as follows: `assets/mip-N` (where **N** is to be replaced with the MIP number). When linking to an image in the MIP, use relative links such as `../assets/mip-1/image.png`.

## MIP Header Preamble

Each MIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` mip:` *MIP number* (this is determined by the MIP editor)

` title:` *MIP title*

` author:` *a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.*

` discussions-to *:` *a url pointing to the official discussion thread*

` status:` *Draft / Last Call / Accepted / Final / Active / Abandoned / Rejected / Superseded*

` review-period-end *:` *date review period ends*

` type:` *Use Case / Technical / Informational / Meta*

` created:` *date created on*

` updated*:` *comma separated list of dates*

` requires *:` *MIP number(s)*

` replaces *:` *MIP number(s)*

` superseded-by *:` *MIP number(s)*

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses or usernames of the authors/owners of the MIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

#### `discussions-to` header

While an MIP is a draft, a `discussions-to` header will indicate the URL where the MIP is being discussed.

No `discussions-to` header is necessary if the MIP is being discussed privately with the author.

As a single exception, `discussions-to` cannot point to GitHub pull requests.

#### `type` header

The `type` header specifies the type of MIP: Use Case, Technical, Meta, or Informational.

#### `created` header

The `created` header records the date that the MIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2020-03-30.

#### `updated` header

The `updated` header records the date(s) when the MIP was updated with "substantial" changes. This header is only valid for MIPs of Draft and Active status.

#### `requires` header

MIPs may have a `requires` header, indicating the MIP numbers that this MIP depends on.

#### `superseded-by` and `replaces` headers

MIPs may also have a `superseded-by` header indicating that an MIP has been rendered obsolete by a later document; the value is the number of the MIP that replaces the current document. The newer MIP must have a `replaces` header containing the number of the MIP that it rendered obsolete.

## Auxiliary Files

If your MIP requires images or other auxiliary files, they should be included in a subdirectory of the `assets` folder for that MIP as follows: `assets/mip-N` (where **N** is to be replaced with the MIP number). When linking to a file in the MIP, use relative links such as `../assets/mip-1/image.png`.

## Transferring MIP Ownership

It occasionally becomes necessary to transfer ownership of MIPs to a new hero. In general, we'd like to retain the original author as a co-author of the transferred MIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the MIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the MIP. We try to build consensus around an MIP, but if that's not possible, you can always submit a competing MIP.

If you are interested in assuming ownership of an MIP, send a message asking to take over, addressed to both the original author and the MIP editor. If the original author doesn't respond to email in a timely manner, the MIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

## MIP Editors

The current MIP editors are

* Yury Glushkov ([@PaterSantyago](https://github.com/PaterSantyago))
* Sergey Nesterov ([@starkmsu](https://github.com/starkmsu))
* Andrei Tarutin ([@tarurar](https://github.com/tarurar))

## Core Team

The current Core Team members are

* Sergey Nesterov ([@starkmsu](https://github.com/starkmsu))
* Yury Glushkov ([@PaterSantyago](https://github.com/PaterSantyago))
* Andrei Tarutin ([@tarurar](https://github.com/tarurar))
* Giorgi Mukhigulashvili ([@thelittledevops](https://github.com/thelittledevops))


## MIP Editor Responsibilities

For each new MIP that comes in, an editor does the following:

- Read the MIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the MIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

If the MIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the MIP is ready for the repository, the MIP editor will:

- Assign an MIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this MIP)

- Merge the corresponding pull request

- Send a message back to the MIP author with the next step.

Many MIPs are written and maintained by developers with write access to the OpenVASP codebase. The MIP editors monitor MIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on MIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [Ethereum's EIP-1] written by Martin Becze, Hudson Jameson, and others. In many places text (which is in order based on [Bitcoin's BIP-1] and [Python’s PEP-0001]) was simply copied and modified. Authors of EIP-1, BIP-0001 and PEP-0001 are not responsible for its use in the MAVN Improvement Process, and should not be bothered with technical questions specific to OpenMAVN or the MIP. Please direct all comments to the MIP editors.

See [the revision history for further details](https://github.com/OpenVASP/MIPs/commits/master/MIPS/mip-1.md), which is also available by clicking on the History button in the top right of the MIP.

## Bibliography

1. [Bitcoin's BIP-0001]
2. [Bitcoin's BIP-0001]
3. [pull request]
4. [Python's PEP-0001]
5. [markdown]
6. [the Issues section of this repository]
7. [the OpenMAVN Slack workspace]  
8. [the OpenMAVN MIPs Telegram group]

[Bitcoin's BIP-0001]: https://github.com/bitcoin/bips
[Ethereum's EIP-1]: https://github.com/ethereum/EIPs
[pull request]: https://github.com/OpenMAVN/MIPs/pulls
[Python's PEP-0001]: https://www.python.org/dev/peps/
[markdown]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[the Issues section of this repository]: https://github.com/OpenMAVN/MIPs/issues
[the OpenMAVN Slack workspace]: https://join.slack.com/t/openmavn/shared_invite/zt-d1bku3gj-IUrfs36DHYkJ4D~l~DgUbQ
[the OpenMAVN MIPs Telegram group]: https://t.me/joinchat/GEXIWVWhA8Bo7Oiozw1WmQ

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).