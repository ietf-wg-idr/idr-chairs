# IDR Working Group Document Pipeline
This repository tracks the status and tasks for the [IETF Inter-domain routing Working Group](https://datatracker.ietf.org/wg/idr/about/) that standardizes [BGP](https://en.wikipedia.org/wiki/Border_Gateway_Protocol), the Border Gateway Protocol.  IDR also maintains a [wiki](https://wiki.ietf.org/group/idr) where various IDR work is done, including tracking [implementation reports](https://wiki.ietf.org/group/idr) needed for advancing documents through the IETF process.

This repository focuses on the chairs' project management tasks, including overall working group status.

IDR follows the Internet Standards Process documented in [BCP 9](https://datatracker.ietf.org/doc/bcp9/).  This repository provides visibility in how IDR implements some of the stages of that process.

The [status.md](status.md) file tracks the active status of the Working Group.  The goal of this file is to provide a view of specific active tasks for the pipeline of the Working Group and where they are at in that pipeline.

The chairs are experimenting with Github **issues** in this repository might be leveraged to track specific working group-wide tasks.

## Working Group Chair's TODO queue

Actions by the chairs are required in many cases to move a document through the document pipeline.  These actions include things such as reviews, running adoption calls, last calls, and interactions with authors and other IETF Working Groups.  The chairs make every attempt to not be the blocking factor in advancement of documents throughout the pipeline, but some tasks cannot be delegated.

The IDR chairs and WG secretary meet approximately on a weekly basis to determine active status of the working group pipeline tasks and to pick next actions for various documents.  It's the goal of the chairs to track the status of the working group and the required actions in this repository.  

Targeted **deadlines** are tracked as "[ETA](https://en.wikipedia.org/wiki/Estimated_time_of_arrival)"s in the document.  Unfortunately, these deadlines are often aspirational as other work may disrupt the targeted time.  The goal remains to provide a sense to the working group what the current status of the work is.

This **status** is tracked in the following ways:

- Designated document **shepherds** are tracked in the various documents in this repository, including the main status page.  
- The chairs attempt to provide a high level overview of their next tasks in the [chair-tasks.md](chair-tasks.md) file.

The chairs are experimenting with tracking certain types of tasks as **Github issues**.  At the moment, the files are the canonical way to monitor working group and chair status.

## BGP-related Technologies

IDR standardizes several different BGP related technologies, and assists in the review of other IETF uses of BGP:

- **Core** BGP protocol components and extensions leveraged by the other technologies.
- **Flowspec**, defined by [RFC 8955](https://datatracker.ietf.org/doc/rfc8955/), et seq., which provides for the distribution of traffic flow specifications into BGP.  These are used for, among other things, providing distributed firewall rule distribution for mitigating distributed denial of service (DDoS) attacks.
- **Link-State** (BGP-LS), defined by [RFC 9552](https://datatracker.ietf.org/doc/rfc9552/), which distributes link state information into BGP and is leveraged by other technologies such as Segment Routing and link-state vector routing (LSVR) standardized by the [LSVR Working Group](https://datatracker.ietf.org/wg/lsvr/about/).
- **Segment Routing**, which uses BGP to distribute routing state for segment routing standardized by the [SPRING Working Group.](https://datatracker.ietf.org/wg/spring/about/)

BGP technologies standardized in other IETF Working Groups and not tracked directly in this repository, include:

- [BESS](https://datatracker.ietf.org/wg/bess/about/), which standardizes BGP services such as Layer 3 and Multicast VPNs signaled over BGP.
- [GROW](https://datatracker.ietf.org/wg/grow/about/), the global routing-operations Working Group.  GROW standardizes the BGP Monitoring Protocol (BMP)
- [LSVR](https://datatracker.ietf.org/wg/lsvr/about/), link-state vector routing.

## IDR Document Pipeline

The status of a document in the IDR pipeline will be reflected by the document's [WG state in the datatracker](https://datatracker.ietf.org/doc/help/state/draft-stream-ietf/).

### Pre-adoption pile

- Documents that either have requested adoption, or are under evaluation for adoption are placed in an adoption file covering the relevant BGP technology.
- *Early reviews* are done on these pre-adoption documents by the chairs, BGP directorate, and other parties.
- The pre-adoption files attempts to track the suitability of the document for adoption, and where the document may be in the *adoption queue*.
- Documents that are suitable for adoption may be marked in the IETF datatracker as "*Candidate for WG Adoption*".

### Adoption queue

- Documents where the authors have requested adoption and have been evaluated for suitability for adoption are announced to the Working Group and placed in the In-Progress Adoption Call list in the main status file.
- Documents undergoing adoption will be marked as "*Call For Adoption By WG Issued*" in the datatracker.

### Active documents

- These documents are not tracked in this repository.  Instead they are covered by the [IETF datatracker for IDR](https://datatracker.ietf.org/wg/idr/documents/) and will have the WG state "*Adopted by a WG*".
- The document authors and the working group advance the document through edits and discussion on the IDR mailing list.

### Working Group last call (WGLC)

- When the authors of a document believe the document is ready to advance to publication as an RFC, they request last call for the document.
- Documents that are under consideration for last call are added to a technology-specific file for tracking.
- These files cover high level summaries of the suitability of the document to proceed to last call.  This suitability may be evaluated by chair, BGP directorate, or other review.
- Issues with the document are ideally tracked in a Github repository for that document, if one exists.  If not, IDR will create an IDR Github repository solely for tracking the issues for the document and the resolution status of those issues.
- Once the document is ready for advancing to last call, it is moved out of the technology specific file to the main status page to track an active last call.  The WG Status is set to "*In WG Last Call*".
  - Documents that do not pass last call may revert to the technology specific files and try again later once issues identified during the last call have been addressed.
  - Tightly iterating responses from the author that are part of last call discussion may cause the document to stay in the active status and extend the call at the discretion of the chairs.
- A successful last call for the document will have the document move into the "*WGLC - Waiting for Shepherd Writeup*" portion of the status file.  The document's Working Group state will be set to "*WG Consensus: Waiting for Write-Up*".

### Document submission to the IESG or other streams.

- Once the shepherd writeup is completed, the document is submitted to the for publication  as an RFC- typically to the IESG.  The document's Working Group state is set to "*Submitted to IESG for Publication*".
- This process is often iterative with the authors.  This may include feedback from the IDR Area Director or once past AD-review, the entirety of the IESG.  High level status is tracked in the main status file.

### At the RFC Editor

- The document is almost at the finish line.  The high level status of the document, including pending next actions, is tracked in the main status file.

### IANA Actions

- Documents at various parts of their life cycle may require interaction with IANA.  This typically includes either early assignment, or at publication assignment of BGP or other code points in an IANA-maintained registry.
- The state of the IANA interaction is tracked in the main status file.  This primarily covers early allocations.  Final allocations are often done as part of the RFC Editor process.

