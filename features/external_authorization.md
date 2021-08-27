[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:** Better External Authorization

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):** @yangminzhu

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:**

[//]: # (A short description of the feature. One or two sentences maximum.)


**Design Docs:**

[//]: # (Design docs for feature)

https://docs.google.com/document/d/1V4mCQCw7mlGp0zSQQXYoBdbKMDnkPOjeyUb85U07iSI/edit

**Relevant Documentation:**

[//]: # (Links to relevant documentation for feature)

* https://istio.io/latest/blog/2021/better-external-authz/
  
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

---

## Alpha

### Requirements: 

**Design**

- [x] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. 

> Design doc already approved: https://docs.google.com/document/d/1V4mCQCw7mlGp0zSQQXYoBdbKMDnkPOjeyUb85U07iSI/edit

**Config**

- [x] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

> The user needs to configure extension provider and authz policy to enable the feature, see task in istio.io/latest/docs/tasks/security/authorization/authz-custom

**Docs**

- [x] Reference docs are published to preliminary.istio.io or the Istio wiki.

> The reference doc of the new CUSTOM action is published at https://preliminary.istio.io/latest/docs/reference/config/security/authorization-policy/#AuthorizationPolicy-Action

- [x] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats.

> The task page of the feature is published at https://istio.io/latest/docs/tasks/security/authorization/authz-custom/

- [ ] Release notes entries added as appropriate

> This is targeting 1.12 release, will add corresponding release note later.

- [x] Upgrade notes entries added as appropriate

> The alpha promotion of the feature is fully compatible with the experimental version, we do not need upgrade notes.

**Tests**

- [x] Automated integration tests cover core use cases with the feature enabled.

> The feature is covered by the e2e tests: https://github.com/istio/istio/blob/2dd90cefe1ac405ba8bf96a66a35af61e4fd99ae/tests/integration/security/authorization_test.go#L1309

- [x] When disabled, the feature does not affect system stability or performance. 

> No ext-authz filter generated when disabled.


**API**

- [x] Initial API review.

> The alpha promotion includes a few API changes based on customer feedback, the change has been approved: https://github.com/istio/api/pull/1926.

**Approvals**

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.

> Promoting of this feature to alpha is on the security WG roadmap for Istio 1.12 release, see https://docs.google.com/document/d/1KEqes4TiyfNnX8DF8TEilyRTMTwsLD9UNMPrm86PgmU/edit#heading=h.tmxzuzkx5jj2

- [ ] The TOC has reviewed and approved promotion of the feature as part of the roadmap for a release.

> To be reviewed.

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
- [ ] Documentation on istio.io includes samples/tutorials. 
- [ ] Documentation on istio.io includes appropriate glossary entries. 
- [ ] All new documentation containing user actions includes istio.io tests.
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

- [ ] Feature has no known major issues.

**Approvals**

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature.  
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


