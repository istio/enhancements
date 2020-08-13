---
name: Alpha Feature Requirements
about: Requirements for promoting a feature to alpha
---

This page lists the requirements for promoting a feature to alpha. Please check off and document the steps as they are completed.

**Feature Name:** 
--- 

### Requirements: 

**Design**

- [ ] Requires approved RFC in order to merge. 

**Config**

- [ ] Requires explicit user action to enable (e.g. a config field, config resource, or installation action). 

**Docs**

- [ ] Reference docs are published to istio.io. 
- [ ] Basic feature docs are published on istio.io describing what the feature does, how to use it, and any caveats. 
- [ ] Whenever possible, documentation has automated istio.io tests written. 
- [ ] A reference to the design doc/issue is published on istio.io. 
- [ ] Release notes entries added as appropriate
- [ ] Upgrade notes entries added as appropriate

**Tests**

- [ ] Test coverage is >= 70%
- [ ] Integration tests cover core use cases with the feature enabled. 
- [ ] When disabled, the feature does not affect system stability or performance. 
- [ ] Feature coverage and test plans written and approved


**Performance**
- [ ] Performance requirements assessed as part of the design. 

**API**

- [ ] (Optional) Initial API review.

**Promotion**

- [ ] Reviewed by the appropriate workgroup and added to the workgroup roadmap.
- [ ] Approved by TOC.
