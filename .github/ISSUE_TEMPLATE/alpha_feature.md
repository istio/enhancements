---
name: Alpha Feature Requirements
about: Requirements for promoting a feature to alpha
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

--- 

### Requirements: 

**Design**

- [ ] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. 

**Config**

- [ ] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

	[Instructions for enabling](insert_your_link_here)

**Docs**

- [ ] [Reference docs](insert_your_link_here) are published to preliminary.istio.io or the Istio wiki.
- [ ] [Basic feature docs](insert_your_link_here) are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 
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
