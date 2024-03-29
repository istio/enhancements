[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:**

JWT Claim Based Routing
[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):**
Aryan Gupta

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:**

Routing based on JWT Claims, only valid for ingress gateway usecases
[//]: # (A short description of the feature. One or two sentences maximum.)


**Design Docs:**

[Claim Based Routing](https://docs.google.com/document/d/1s8Lykf8-KUZTLiG4YMSCHvxBDwZzHlrrHyZ7cJymc_8)

[//]: # (Design docs for feature)


**Relevant Documentation:**

* https://istio.io/latest/docs/tasks/security/authentication/jwt-route/

[//]: # (Links to relevant documentation for feature)

**RFC:**

[//]: # (Link to RFC for feature)
N/A. Design doc presented instead.


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


[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [ ] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature
---

## Alpha

### Requirements: 

**Design**

- [x] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. 

> Design doc already approved: https://docs.google.com/document/d/1s8Lykf8-KUZTLiG4YMSCHvxBDwZzHlrrHyZ7cJymc_8)

**Config**

- [x] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

> The user needs to modify the virtual service to enable this feature - https://istio.io/latest/docs/tasks/security/authentication/jwt-route/

**Docs**

- [x] Reference docs are published to preliminary.istio.io or the Istio wiki.

> The task page of the feature is published at https://istio.io/latest/docs/tasks/security/authentication/jwt-route/

- [x] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 

> A task has been added

- [x] Release notes entries added as appropriate

> Targeting for 1.16 release, will add it later when required

- [x] Upgrade notes entries added as appropriate

> The alpha promotion of the feature is fully compatible with the experimental version, we do not need upgrade notes.

**Tests**

- [x] Automated integration tests cover core use cases with the feature enabled. 
- [x] When disabled, the feature does not affect system stability or performance. 

**API**

- [ ] Initial API review.

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [x] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.

**Promotion**

[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [x] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature

---

## Beta

### Requirements: 

**Design**

- [] Design doc describing the intention of the feature, how it will be
	implemented, and any thoughts on how to test the feature has been approved by
	relevant work group leads
- [] Feature coverage and test plans written and approved.

**Docs** 

- [ ] Documentation on istio.io includes performance expectations; may have caveats. 
- [] Documentation on istio.io includes samples/tutorials.
- [] Documentation on istio.io includes appropriate glossary entries.
- [] All new documentation containing user actions includes istio.io tests.
- [] Release notes have been added.
- [] Upgrade notes have been added.

**Tests**

- [] Integration tests cover feature edge cases
- [] End-to-end tests cover samples/tutorials
- [] Fixed issues have tests to prevent regressions
- [ ] Stability/stress test suite includes coverage for the feature.

**Performance**

- [ ] Feature coverage and test plans written and approved 
- [ ] Tests exist with the feature enabled that can be integrated with our automated performance testing.

**API**

- [ ] TOC has reviewed the API and determined it to be complete. 

**Tooling**

- [ ] Any necessary tooling to use/debug the feature has been implemented and is complete. 

**Bugs**

- [] Feature has no known major issues.

**Approvals**

- [] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature.  
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
	road map for a release.


**Promotion**

[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature
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
- [ ] The [supportability review panel](https://docs.google.com/document/d/1w0epyFhhDSf_TwFEfa_lrn1v61mXNJKpEp_kUgp4sSc/edit#) has reviewed the feature in order to find any supportability concerns.  
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.


**Promotion**

[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [ ] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature
