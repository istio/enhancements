[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:** Configuring Gateway Network Topology

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):** @jacob-delgado

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:**

[//]: # (A short description of the feature. One or two sentences maximum.)


**Design Docs:**

[//]: # (Design docs for feature)


**Relevant Documentation:**

[//]: # (Links to relevant documentation for feature)

* https://istio.io/latest/docs/ops/configuration/traffic-management/network-topologies/

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

- [x] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. 

Not needed as it was approved in 1.6 and was approved in istio/api. Design only affects meshConfig which means it cannot be promoted past Beta anyway.

**Config**

- [x] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

> istio api: [istio/api#1394](https://github.com/istio/api/pull/1394) and [istio/api#1403](https://github.com/istio/api/pull/1403)
istio/istio: [istio/istio#23292](https://github.com/istio/istio/pull/23292)

**Docs**

- [x] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [x] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 

https://istio.io/latest/docs/ops/configuration/traffic-management/network-topologies/

- [x] Release notes entries added as appropriate
- [x] Upgrade notes entries added as appropriate

**Tests**

- [x] Automated integration tests cover core use cases with the feature enabled. 
	* https://github.com/istio/istio/pull/30500
	* https://github.com/istio/istio/pull/27861
- [x] When disabled, the feature does not affect system stability or performance. 

**API**

- [x] Initial API review.

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [x] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.
    * Cleaned up docs: https://github.com/istio/istio.io/pull/9090
    * Automated test for Network topology: https://istio.io/latest/docs/ops/configuration/traffic-management/network-topologies/ (https://github.com/istio/istio.io/pull/9096).

---

## Beta

### Requirements: 

**Design**

- [ ] Design doc describing the intention of the feature, how it will be
	implemented, and any thoughts on how to test the feature has been approved by
	relevant work group leads
- [ ] Feature coverage and test plans written and approved.

**Docs** 

- [ ] Documentation on istio.io includes performance expectations; may have caveats. 
- [x] Documentation on istio.io includes samples/tutorials. 
- [x] Documentation on istio.io includes appropriate glossary entries. 
- [x] All new documentation containing user actions includes istio.io tests.
- [ ] Release notes have been added. 
- [ ] Upgrade notes have been added. 

**Tests**

- [ ] Integration tests cover feature edge cases
- [ ] End-to-end tests cover samples/tutorials
- [ ] Fixed issues have tests to prevent regressions
- [ ] Stability/stress test suite includes coverage for the feature.

**Performance**

- [ ] Feature coverage and test plans written and approved 
- [ ] Tests exist with the feature enabled that can be integrated with our automated performance testing.

**API**

- [ ] TOC has reviewed the API and determined it to be complete. 

**Tooling**

- [ ] Any necessary tooling to use/debug the feature has been implemented and is complete. 

**Bugs**

- [x] Feature has no known major issues.

**Approvals**

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature. N/A. Feature is too minor to involve panel
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
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


