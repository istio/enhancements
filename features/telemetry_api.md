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

[//]: # (The name of the feature, e.g. Multiple control planes)

Configurable Telemetry Production

**Primary lead(s):**

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

douglas-reid

**Short description:**

[//]: # (A short description of the feature. One or two sentences maximum.)

The Telemetry API enables control of the telemetry production within a mesh.

**Design Docs:**

[//]: # (Design docs for feature)

- [Proposal: Telemetry API](https://docs.google.com/document/d/1pTFVzGii7sB4uALMsrUN4ALFc0J7vI2UyBnJpP_bsgU/edit#heading=h.gryauiau89tc)
- [Telemetry API: Metrics - Key Decisions](https://docs.google.com/document/d/1ZdzLM5E6oY1a6MjE9SRnnpMyrANjGx4y_Opg290Ol-M/edit?usp=sharing&resourcekey=0-uERWDjv-m4Ccyr8eP2mgxg)
- [Logging Configuration with Telemetry API](https://docs.google.com/document/d/1m7F5Tz0E-n7P3Qmq7ecCx-ykhA_njlxGFNx8LIMPBBg/edit?usp=sharing&resourcekey=0-JxDkXLnu2L8xtsAHDXxyCQ)
- [Telemetry API Migration](https://docs.google.com/document/d/1FMvwyoooGeiACf9b7R0A6iJyB6ZuiP7hv5-XDmXtHLo/edit?usp=sharing)


**Relevant Documentation:**

[//]: # (Links to relevant documentation for feature)

- [Telemetry API](https://istio.io/latest/docs/tasks/observability/telemetry/)

**RFC:**

[//]: # (Link to RFC for feature)

- [RFC: Telemetry API](https://docs.google.com/document/d/1Tv-A2eftrNQrouMsdBLiHdILIwVN3n2c7RJYNVuv7GY/edit#)
- [RFC: Telemetry API Scope](https://docs.google.com/document/d/1PfmqSpO5c3jCdQ__DppPYlW9IzupSkA5WhuOTGGwlK8/edit#)
- [Telemetry v1 API](https://docs.google.com/document/d/16A-E-30txN5Y2V_9qrDNpVC3lT7P6aa_3Qdg6_4t5Sg/edit)

---

## Experimental

### Requirements:

[//]: # (All information in this section is mandatory for promotion. Please modify the links in this)
[//]: # (section.)

- [X] [User stories](https://docs.google.com/document/d/1pTFVzGii7sB4uALMsrUN4ALFc0J7vI2UyBnJpP_bsgU/edit#bookmark=id.dp9fgncrklih) reviewed in a work group meeting.

[//]: # (User stories are a way to communicate user value. User stories follow the style)
[//]: # (as a [type of user], I want [an action] so that [a benefit/a value]. Istio currently has no user)
[//]: # (story template. Maybe you can make one?)

[//]: # (User stories must be presented in a work group meeting. They need no approval and are later integrated)
[//]: # (into the RFCs, which do need approval for alpha. You may find value to negotiate within the work group where the)
[//]: # (user stories are presented to help clarify the user stories.)

- [X] [RFC Authored] - [RFC: Telemetry API](https://docs.google.com/document/d/1Tv-A2eftrNQrouMsdBLiHdILIwVN3n2c7RJYNVuv7GY/?usp=sharing).

[//]: # (An RFC is mandatory to graduate to experimental. The RFC does not have to be reviewed in a work group)
[//]: # (meeting to graduate to experimental.)

- [X] [Documentation](https://istio.io/latest/docs/tasks/observability/telemetry/) for enabling and using the feature.

[//]: # (The documentation instructions may exist on the developer wiki or the team drive. They may include instructions)
[//]: # (for building running a `istioctl experimental command`, or using the preview profile,)
[//]: # (or any other relevant information.)

- [X] Feedback plan: utilize GitHub issues, forum discussions, and direct engagements.

[//]: # (This may include user feedback meetings, discuss.istio.io conversations, GitHub issues, or mailing lists.)

- [X] Disabled by default.

- [X] No impact on performance when the feature is disabled.


[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [X] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature
---

## Alpha

### Requirements:

**Design**

- [X] RFC has been approved describing the intention of the feature as well as the user stories behind the feature.

**Config**

- [X] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action).

> Link to instructions for enabling

**Docs**

- [X] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [X] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats.
- [X] Release notes entries added as appropriate
- [X] Upgrade notes entries added as appropriate

**Tests**

- [X] Automated integration tests cover core use cases with the feature enabled.
- [X] When disabled, the feature does not affect system stability or performance.

**API**

- [X] Initial API review.

**Approvals**

- [X] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [X] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.

**Promotion**

[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [X] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature

---

## Beta

### Requirements:

**Design**

- [X] Design doc describing the intention of the feature, how it will be
	implemented, and any thoughts on how to test the feature has been approved by
	relevant work group leads
- [X] Feature coverage and test plans written and approved.

**Docs**

- [ ] Documentation on istio.io includes performance expectations; may have caveats.
- [X] Documentation on istio.io includes samples/tutorials.
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

- [X] Feature coverage and test plans written and approved
- [ ] Tests exist with the feature enabled that can be integrated with our automated performance testing.

**API**

- [x] TOC has reviewed the API and determined it to be complete.

**Tooling**

- [ ] Any necessary tooling to use/debug the feature has been implemented and is complete.

**Bugs**

- [x] Feature has no known major issues.

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature OR a WG has decided one is not required.
- [x] The TOC has reviewed and approved promotion of the feature as part of the
	road map for a release.


**Promotion**

[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [x] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature
---

## Stable

### Requirements:

**Performance**

- [ ] Latency, throughput, and scalability are quantified and documented on
	istio.io.

**Bugs**

- [ ] Feature has no known major issues.

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The [supportability review panel](https://docs.google.com/document/d/1w0epyFhhDSf_TwFEfa_lrn1v61mXNJKpEp_kUgp4sSc/edit#) has reviewed the feature in order to find any supportability concerns OR a WG has decided one is not required.
- [x] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.


**Promotion**

[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [x] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature
