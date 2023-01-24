[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:** Helm v3 support

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):** Neeraj Poddar

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:** Helm v3 installation support in Istio

[//]: # (A short description of the feature. One or two sentences maximum.)

**Relevant Documentation:**

* preliminary.istio.io/latest/docs/setup/install/helm
* preliminary.istio.io/latest/faq/setup

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
https://docs.google.com/document/d/1upInT_Qe3-CU2ig_XnUNjP2wLyBr6ImpJfMXvz-BYec/edit#heading=h.h4dnnbkwzgzw

**Config**

- [x] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

> https://preliminary.istio.io/latest/docs/setup/install/helm/

**Docs**

- [x] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [x] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 
- [x] Release notes entries added as appropriate
- [x] Upgrade notes entries added as appropriate
**N/A** as only upgrades from 1.8.x and above are supported.

**Tests**

- [x] Automated integration tests cover core use cases with the feature enabled. 
https://github.com/istio/istio/tree/1ec9f765e3b938b519e393c8a04675cfc6d0470b/tests/integration/helm

- [x] When disabled, the feature does not affect system stability or performance. 

**API**

- [x] Initial API review.
Helm install/upgrade commands are well known APIs. Configuring options via Helm values is considered experimental and will be matured in 1.9 and above.

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
- [x] Feature coverage and test plans written and approved.

**Docs** 

- [x] Documentation on istio.io includes performance expectations; may have caveats. 
- [x] Documentation on istio.io includes samples/tutorials. 
[Helm Documentation](https://preliminary.istio.io/latest/docs/setup/install/helm/) has been enhanced to include more usecases.
- [x] Documentation on istio.io includes appropriate glossary entries. 
- [x] All new documentation containing user actions includes istio.io tests.
[Helm Documentation](https://preliminary.istio.io/latest/docs/setup/install/helm/) has tests enabled
- [x] Release notes have been added. 
- [x] Upgrade notes have been added. 

**Tests**

- [x] Integration tests cover feature edge cases
- [x] End-to-end tests cover samples/tutorials
[Helm integration tests](https://github.com/istio/istio/tree/master/tests/integration/helm) have been simplified to make upgrade tests easier.
- [x] Fixed issues have tests to prevent regressions
- [ ] Stability/stress test suite includes coverage for the feature.
N/A

**Performance**

- [ ] Feature coverage and test plans written and approved 
N/A
- [x] Tests exist with the feature enabled that can be integrated with our automated performance testing.

**API**

- [x] TOC has reviewed the API and determined it to be complete. 

**Tooling**

- [x] Any necessary tooling to use/debug the feature has been implemented and is complete. 
[Helm linting](https://github.com/istio/installer/pull/426) has been enabled.

**Bugs**

- [x] Feature has no known major issues.
Majors issues and enhancements were tracked [here](https://github.com/istio/istio/issues/42565) and is now complete.

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature.  
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


