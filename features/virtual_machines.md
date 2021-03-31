[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:** Virtual Machines

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):** John Howard

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:** Virtual Machine Support for Istio

[//]: # (A short description of the feature. One or two sentences maximum.)

**Design Docs:**

*  docs.google.com/document/d/1aMdRacznhGUsBWTx-KNzYEcEPKDgVtVQBLcRCBAMTb8
* docs.google.com/document/d/1VDV4-prbMbzW06hslfp12sn7V6oUvnIAst6mT6FtSWc
* docs.google.com/document/d/10TyPy-6bOs0_7JljGpc2RneDdsaR9GktjwwaaVbz6fs
* docs.google.com/document/d/1G4s_PrmvkwCKoH_kXVeSUAszsaj3ZfpIlraSdeTSPKU
* docs.google.com/document/d/1BuwOX6D30Yy6lTvj4RHwLzcUoaAu61pAdtKnLx312ec
* docs.google.com/document/d/1-612Sgz_skeoX44dw3MU6Z8ONgq1f29wLUI9zggyLec
* docs.google.com/document/d/1QReA8XjWrWTnErQYPZUdPA5d2O6fc3VkLWr47hY0Nbg
* docs.google.com/document/d/1-RVOpCGbcDdr-yM4UrT0WgfHZglgQZlPL1d1aZbqEbk

**Relevant Documentation:**

  * preliminary.istio.io/latest/docs/setup/install/virtual-machine
    
  * preliminary.istio.io/latest/docs/examples/virtual-machines

**RFC:** 

N/A. Design docs presented instead. 

---

## Experimental

### Requirements:

[//]: # (All information in this section is mandatory for promotion. Please modify the links in this)
[//]: # (section.)

- [ ] [User stories](insert_your_link_here) reviewed in a work group meeting.

[//]: # (User stories are a way to communicate user value. User stories follow the style)
[//]: # (as a [type of user], I want [an action] so that [a benefit/a value]. Istio currently has no user)
[//]: # (story template. Maybe you can make one?)

[//]: # (User stories must be presented in a work group meeting. They need no approval and are later integrated)
[//]: # (into the RFCs, which do need approval for alpha. You may find value to negotiate within the work group where the)
[//]: # (user stories are presented to help clarify the user stories.)

- [x] [RFC Authored] - [create an RFC using template](https://docs.google.com/document/d/1ewJoCcw5-04crH-M0xw4zFxz1cfwVCPnNyW4K3m4Yyc/template/preview).

[//]: # (An RFC is mandatory to graduate to experimental. The RFC does not have to be reviewed in a work group)
[//]: # (meeting to graduate to experimental.)

- [ ] [Documentation](insert_your_link_here) for enabling and using the feature.

[//]: # (The documentation instructions may exist on the developer wiki or the team drive. They may include instructions)
[//]: # (for building running a `istioctl experimental command`, or using the preview profile,)
[//]: # (or any other relevant information.)

- [ ] [Feedback plan](insert_your_link_here).

[//]: # (This may include user feedback meetings, discuss.istio.io conversations, GitHub issues, or mailing lists.)

- [ ] Disabled by default.

- [ ] No impact on performance when the feature is disabled.

---

## Alpha

### Requirements: 

**Design**

- [x] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. **N/A** design doc presented instead

**Config**

- [x] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). **N/A** no longer required as feature is beta at time of evaluation. 

**Docs**

- [x] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [x] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 
- [x] Release notes entries added as appropriate
- [x] Upgrade notes entries added as appropriate

**Tests**

- [x] Automated integration tests cover core use cases with the feature enabled. 
- [x] When disabled, the feature does not affect system stability or performance. 

**API**

- [x] Initial API review.

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [x] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.

---

## Beta

### Requirements: 

**Design**

- [x] Design doc describing the intention of the feature, how it will be
	implemented, and any thoughts on how to test the feature has been approved by
	relevant work group leads
**YES**: see links above. The design docs cover every working group; this feature has been collaborated on by all groups.
- [x] Feature coverage and test plans written and approved.

**Docs** 

- [x] Documentation on istio.io includes performance expectations; may have caveats. 
**YES**: VMs do not have a different performance profile from Kubernetes pods.
- [x] Documentation on istio.io includes samples/tutorials. 
**YES**: see docs above
- [x] Documentation on istio.io includes appropriate glossary entries. 
**YES**: This feature does not introduce new vocabulary.
- [x] All new documentation containing user actions includes istio.io tests.
**YES** the docs have tests
- [x] Release notes have been added. 
**YES** Individual features have release notes
- [x] Upgrade notes have been added. 
**YES** No upgrade notes have been needed as these are new features.

**Tests**

- [x] Integration tests cover feature edge cases 
**YES** we have VMs as part of networking, security, and telemetry tests.
- [x] End-to-end tests cover samples/tutorials
**YES** docs all have tests and are extensive
- [x] Fixed issues have tests to prevent regressions
**YES** we have included regression tests for various `WorkloadEntry` bugs and for certificate rotation bugs.
- [x] Stability/stress test suite includes coverage for the feature.
**YES** we have added VM

**Performance**

- [x] Feature coverage and test plans written and approved 
- [x] Tests exist with the feature enabled that can be integrated with our automated performance testing.
**YES** istio/tools#1432

**API**

- [x] TOC has reviewed the API and determined it to be complete. 
**YES**: all APIs (workload entry, workload group) were approved during their introduction. 

**Tooling**

- [x] Any necessary tooling to use/debug the feature has been implemented and is complete. 
**YES** istioctl has commands to bootstrap VMs and has support for common commands like `proxy-config` and `proxy-status`.

**Bugs**

- [x] Feature has no known major issues.

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
  - [x] Environments
  - [x] Networking
  - [x] Security
  - [x] Telemetry
- [x] The supportability review panel has reviewed promotion of the feature.  
[Meeting results](https://docs.google.com/document/d/1mSB5r2RwegClg5TY3m5yr5Cgf6mvtvqRFmrfmX1DU2c/edit#). Some documentation updates are blocking.
- [x] The TOC has reviewed and approved promotion of the feature as part of the
	road map for a release.

---

## Stable

### Requirements: 

**Performance**

- [ ] Latency, throughput, and scalability are quantified and documented on
	istio.io. 

**Bugs**

- [ ] Feature has no known major issues. 

**Approvals**

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature.  
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.


