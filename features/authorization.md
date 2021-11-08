[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

Istio Authorization

[//]: # (All information in this section is mandatory.)

**Feature name:**

Istio Authorization Policy

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):**

Yangmin Zhu (ymzhu@google.com)
[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:**

Istio Authorization provides access control for workloads in the mesh at the namespace, mesh and workload level.

[//]: # (A short description of the feature. One or two sentences maximum.)


**Design Docs:**
[Istio Authorization Policy v1beta1 Enforcement](https://docs.google.com/document/d/1EUmmYiUUuro_509NFK7NTxvbHJ7ehm9G8fCAaiYa3aw/edit#heading=h.hb4h97m77jmk)

[//]: # (Design docs for feature)


**Relevant Documentation:**

[//]: # (Links to relevant documentation for feature)

**RFC:**

[//]: # (Link to RFC for feature)


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

- [ ] [RFC Authored] - [create an RFC using template](https://docs.google.com/document/d/1ewJoCcw5-04crH-M0xw4zFxz1cfwVCPnNyW4K3m4Yyc/template/preview).

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

- [X] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. 

**Config**

- [X] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

> Link to instructions for enabling

**Docs**

- [X] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [X] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 
- [X] Release notes entries added as appropriate
- [X] Upgrade notes entries added as appropriate

**Tests**

- [X] Automated integration tests cover core use cases with the feature enabled. 
- [X] When disabled, the feature does not affect system stability or performance. 

**API**

- [X] Initial API review.

**Approvals**

- [X] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [X] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.

---

## Beta

### Requirements: 

**Design**

- [X] Design doc describing the intention of the feature, how it will be
	implemented, and any thoughts on how to test the feature has been approved by
	relevant work group leads
  [Deny and exclude in AuthorizationPolicy](https://docs.google.com/document/d/1aJ1hffHz9JYGXIM9btnKaWmwVdn1Qg34FJScnDyZPw4/edit#)
  
- [X] Feature coverage and test plans written and approved.

**Docs** 

- [X] Documentation on istio.io includes performance expectations; may have caveats.
  [Large Scale Security Policy Performance Tests](https://istio.io/latest/blog/2020/large-scale-security-policy-performance-tests/)
  
- [X] Documentation on istio.io includes samples/tutorials. 
- [ ] Documentation on istio.io includes appropriate glossary entries. 
- [X] All new documentation containing user actions includes istio.io tests.
- [X] Release notes have been added. 
- [X] Upgrade notes have been added. 

**Tests**

- [X] Integration tests cover feature edge cases
- [X] End-to-end tests cover samples/tutorials
- [X] Fixed issues have tests to prevent regressions
- [X] Stability/stress test suite includes coverage for the feature.

**Performance**

- [X] Feature coverage and test plans written and approved 
- [X] Tests exist with the feature enabled that can be integrated with our automated performance testing.

**API**

- [X] TOC has reviewed the API and determined it to be complete. 

**Tooling**

- [ ] Any necessary tooling to use/debug the feature has been implemented and is complete. 

**Bugs**

- [X] Feature has no known major issues.

**Approvals**

- [X] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [X] The supportability review panel has reviewed promotion of the feature.  
- [X] The TOC has reviewed and approved promotion of the feature as part of the
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


