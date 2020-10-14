---
name: Beta Feature Requirements
about: Requirements for promoting a feature to beta
---

[//]: # (The syntax preceeding this line is a comment marker used to help guide the issue author with submission of an issue)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This page lists the requirements for an experimental feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the issue.)

# Feature: 

[//]: # (All information in this section is mandatory for new issue submission.)

**Feature Name:**  

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary Lead(s):**

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:**

[//]: # (A short description of the feature. One or two sentences maximum.)

**RFC:**

[//]: # (This outlines the ideas for a feature and is used to collect early feedback. See the RFC template here: https://docs.google.com/document/d/1ewJoCcw5-04crH-M0xw4zFxz1cfwVCPnNyW4K3m4Yyc/template/preview)

**Design doc:**

[//]: # (This is used for discussion of design and testing for a feature. See the design doc template here:https://docs.google.com/document/d/16FLQK8uhhic1ovKnnOG3OXJjFKs2aHnSmbximidpKwM/template/preview)

**Relevant Documentation:**

[//]: # (Links to documentation related to the feature. This may be tasks,
# Beta Feature Requirements

This page lists the requirements for promoting a feature to beta. Promotion to beta must meet all requirements for promotion to alpha. Please check off and document the steps as they are completed.

--- 

### Requirements: 

**Design**

- [ ] Design doc has been approved by relevant work group leads

[//]: # (A design doc is mandatory for graduation to beta. The design doc must be
approved by relevant work group leads.)

- [ ] Feature coverage and test plans written and approved.
[//]: # (Feature coverage is required for graduation to beta. More details can be found here: https://github.com/istio/istio/blob/8af80bdf91684d8e517e9e5d57f2c3d8480b11a2/pkg/test/framework/features/README.md)

**Docs** 

- [ ] Documentation on istio.io includes performance expectations; may have caveats. 
- [ ] Documentation on istio.io includes samples/tutorials. 
- [ ] Documentation on istio.io includes appropriate glossary entries. 
- [ ] All new documentation containing user actions includes istio.io tests.

[//]: # (Documentation tests are required in order to be able to confirm that
the documentation is correct across Istio releases. Details on writing Istio
documentation tests can be found here: https://github.com/istio/istio.io/tree/master/tests)

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

[//]: # (In the context of a release, these may be referred to as P0/P1
features. The requirements for meeting this are up to the work group owning the
feature.)

**Approvals**

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature.  
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
	road map for a release.
