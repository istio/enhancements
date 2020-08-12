---
name: Beta Feature Requirements
about: Requirements for promoting a feature to beta
---

This page lists the requirements for promoting a feature to beta. Please check off and document the steps as they are completed.

**Feature Name:** 
--- 

### Requirements: 

**Design**

- [ ] Design doc has been approved

**Config**

- [ ] Can be enabled by default without requiring explicit user action. 

**Docs** 

- [ ] Performance expectations are documented, may have caveats. 
- [ ] Documentation on istio.io includes samples/tutorials. 
- [ ] Documentation on istio.io includes appropriate glossary entries. 
- [ ] Where possible, all documentation changes have istio.io tests written. 
- [ ] Release notes have been added. 
- [ ] Upgrade notes have been added. 

**Tests**

- [ ] Test coverage is >= 80%
- [ ] Integration tests cover feature edge cases
- [ ] End-to-end tests cover samples/tutorials
- [ ] Fixed issues have tests to prevent regressions
- [ ] Ensure that coverage exists for the feature in stability/stress test suite.

**Performance**

- [ ] Feature has baseline performance tests

**API**

- [ ] API has had a thorough API review and is thought to be complete. 

**CLI**

- [ ] Necesssary CLI command has been implemented and are complete. 

**Bugs**

- [ ] Feature has no outstanding P0 bugs

**Promotion**

- [ ] The decision to promote a feature is presented and approved by the workgroup. 
- [ ] The decision to promote a feature is approved by the TOC in the roadmap for a release. 
- [ ] Supportability review addressing support scenario questions that has been discussed in the appropriate workgroup.

