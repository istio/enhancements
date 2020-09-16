---
name: Alpha Feature Requirements
about: Requirements for promoting a feature to alpha
---

# Alpha Feature Requirements

This page lists the requirements for promoting a feature to alpha. Please check off and document the steps as they are completed.

**Feature Name:**  

**Design doc:**

**Relevant Documentation:**

--- 

### Requirements: 

**Design**

- [ ] RFC has been approved. 

**Config**

- [ ] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

```
Link to instructions for enabling
```

**Docs**

- [ ] Reference docs are published to Istio.io, or the Istio wiki.
- [ ] Basic feature docs are published on istio.io describing what the feature does, how to use it, and any caveats. 
- [ ] Release notes entries added as appropriate
- [ ] Upgrade notes entries added as appropriate

**Tests**

- [ ] Automated integration tests cover core use cases with the feature enabled. 
- [ ] When disabled, the feature does not affect system stability or performance. 
- [ ] Feature coverage and test plans written and approved


**Performance**
- [ ] Performance impacts have been measured. Please document any initial performance tests below:

**API**

- [ ] Initial API review.

**Approvals**

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature.  
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.
