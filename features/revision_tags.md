[//]: # (The syntax preceding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:** Revision tags (stable revision labels)

**Primary lead(s):** Sam Naser

**Short description:** Allows use of revisions with stable namespace labels.

**Design Docs:**  [Initial design](https://docs.google.com/document/d/13IGuJg8swtLdNGW5cpF7ZdVkgge8voNp9DWBD93Wb1Q/edit#heading=h.xw1gqgyqs5b), [Default revision](https://docs.google.com/document/d/1k5phTcgJBis4cvPzJAZ5WtHlhWsTmkshMGZ5gca4DVs/edit?resourcekey=0-4Rb5MUYcHJ4rqKMgxc82MQ#heading=h.xw1gqgyqs5b)

**Relevant Documentation:** [Upgrade documentation](https://istio.io/latest/docs/setup/upgrade/canary/#stable-revision-labels-experimental), [Blog post](https://istio.io/latest/blog/2021/revision-tags/) 

---

## Experimental

### Requirements:

[//]: # (All information in this section is mandatory for promotion. Please modify the links in this)
[//]: # (section.)

- [x] [User stories]() reviewed in a work group meeting.

- [x] [RFC Authored](https://docs.google.com/document/d/13IGuJg8swtLdNGW5cpF7ZdVkgge8voNp9DWBD93Wb1Q/edit#heading=h.xw1gqgyqs5b)

- [x] [Documentation](https://istio.io/latest/docs/setup/upgrade/canary/#stable-revision-labels) for enabling and using the feature.

- [ ] [Feedback plan]().

- [x] Disabled by default.

- [x] No impact on performance when the feature is disabled.

---

## Alpha

### Requirements:

**Design**

- [x] RFC has been approved describing the intention of the feature as well as the user stories behind the feature.

**Config**

- [x] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action).

**Docs**

- [x] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [x] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats.
- [x] Release notes entries added as appropriate
- [x] Upgrade notes entries added as appropriate

**Tests**

- [x] Automated integration tests cover core use cases with the feature enabled [Revision Tag Tests](https://github.com/istio/istio/blob/master/tests/integration/pilot/revisions/revision_tag_test.go).
- [x] When disabled, the feature does not affect system stability or performance.

**API**

- [x] Initial API review.


**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature (Environments and UX)
- [x] The TOC has reviewed and approved promotion of the feature as part of the
  roadmap for a release.

---

## Beta

### Requirements:

**Design**

- [x] Design doc describing the intention of the feature, how it will be
  implemented, and any thoughts on how to test the feature have been approved by
  relevant work group leads
- [x] Feature coverage and test plans written and approved (in main design doc).

**Docs**

- [x] Documentation on istio.io includes performance expectations; may have caveats.
- [x] Documentation on istio.io includes samples/tutorials.
- [x] Documentation on istio.io includes appropriate glossary entries.
- [x] All new documentation containing user actions includes istio.io tests.
- [x] Release notes have been added.
- [x] Upgrade notes have been added.

**Tests**

- [x] Integration tests cover feature edge cases
- [x] End-to-end tests cover samples/tutorials
  [Tests](https://github.com/istio/istio/tree/master/tests/integration/pilot/revisions) enhanced to cover more usecases
- [x] Fixed issues have tests to prevent regressions
- [ ] Stability/stress test suite includes coverage for the feature (N/A).

**Performance**

- [x] Feature coverage and test plans written and approved (N/A)
- [x] Tests exist with the feature enabled that can be integrated with our automated performance testing (N/A).

**API**

- [x] TOC has reviewed the API and determined it to be complete.

**Tooling**

- [x] Any necessary tooling to use/debug the feature has been implemented and is complete.

**Bugs**

- [x] Feature has no known major issues.

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature.
- [x] The TOC has reviewed and approved promotion of the feature as part of the
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


