---
name: Beta Feature Requirements
about: Requirements for promoting a feature to beta
---

# Beta Feature Requirements

This page lists the requirements for promoting a feature to beta. Promotion to beta must meet all requirements for promotion to alpha. Please check off and document the steps as they are completed.

**Feature Name:** 

**Design Doc:**

**Alpha Checklist:**

**Relevant Documentation:**

--- 

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
