[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:** Dry-run authorization policy

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):** Yangmin Zhu

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:** 

[//]: # (A short description of the feature. One or two sentences maximum.)

Allow customers to dry-run an authorization policy to test the effect using real traffic without enforcing the policy, reducing the risk of creating or changing the authorization policy.

**Design Docs:**

[//]: # (Design docs for feature)

https://docs.google.com/document/d/1xQdZsEgJ3Ld2qebfT3EJkg2COTtCR1TqBVojmnvI78g/edit#

**Relevant Documentation:**

[//]: # (Links to relevant documentation for feature)

https://istio.io/latest/docs/tasks/security/authorization/authz-dry-run/

**RFC:**

[//]: # (Link to RFC for feature)


---

## Experimental

### Requirements:

[//]: # (All information in this section is mandatory for promotion. Please modify the links in this)
[//]: # (section.)

- [x] [User stories](https://docs.google.com/document/d/1xQdZsEgJ3Ld2qebfT3EJkg2COTtCR1TqBVojmnvI78g/edit#heading=h.pizsw9vhd30a).

[//]: # (User stories are a way to communicate user value. User stories follow the style)
[//]: # (as a [type of user], I want [an action] so that [a benefit/a value]. Istio currently has no user)
[//]: # (story template. Maybe you can make one?)

[//]: # (User stories must be presented in a work group meeting. They need no approval and are later integrated)
[//]: # (into the RFCs, which do need approval for alpha. You may find value to negotiate within the work group where the)
[//]: # (user stories are presented to help clarify the user stories.)

- [x] [RFC Authored]: see the design doc.

[//]: # (An RFC is mandatory to graduate to experimental. The RFC does not have to be reviewed in a work group)
[//]: # (meeting to graduate to experimental.)

- [x] Documentation: https://istio.io/latest/docs/tasks/security/authorization/authz-dry-run/

[//]: # (The documentation instructions may exist on the developer wiki or the team drive. They may include instructions)
[//]: # (for building running a `istioctl experimental command`, or using the preview profile,)
[//]: # (or any other relevant information.)

- [x] Feedback plan: will collect feedback on github, discuss.istio.io and slack.

[//]: # (This may include user feedback meetings, discuss.istio.io conversations, GitHub issues, or mailing lists.)

- [x] Disabled by default: Requires specifying an annotation `istio.io/dry-run: true` on authorization policy to enable the feature)

- [x] No impact on performance when the feature is disabled: No changes to current code flow when disabled

---

## Alpha

### Requirements: 

**Design**

- [ ] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. 

**Config**

- [ ] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

> Link to instructions for enabling

**Docs**

- [ ] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [ ] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 
- [ ] Release notes entries added as appropriate
- [ ] Upgrade notes entries added as appropriate

**Tests**

- [ ] Automated integration tests cover core use cases with the feature enabled. 
- [ ] When disabled, the feature does not affect system stability or performance. 

**API**

- [ ] Initial API review.

**Approvals**

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.

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


