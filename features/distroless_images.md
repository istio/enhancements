[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:** Distroless Images

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):** @howardjohn

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:** support for minimal distroless base images.

[//]: # (A short description of the feature. One or two sentences maximum.)


**Design Docs:**

[//]: # (Design docs for feature)

N/A

**Relevant Documentation:**

[//]: # (Links to relevant documentation for feature)

https://istio.io/latest/docs/ops/configuration/security/harden-docker-images/

**RFC:**

[//]: # (Link to RFC for feature)


---

## Experimental

Experimental steps were skipped as this features was around before enhancements.

## Alpha

### Requirements: 

**Design**

- [ ] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. 

No design doc has been written

**Config**

- [x] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

https://istio.io/latest/docs/ops/configuration/security/harden-docker-images/

**Docs**

All docs are found in https://istio.io/latest/docs/ops/configuration/security/harden-docker-images/

- [x] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [x] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 
- [x] Release notes entries added as appropriate
- [x] Upgrade notes entries added as appropriate

**Tests**


- [x] Automated integration tests cover core use cases with the feature enabled. 

A CI/CD job runs with distroless images enabled on every PR.

- [X] When disabled, the feature does not affect system stability or performance. 

Feature is clearly on or off, cannot impact anything when not used.

**API**

- [x] Initial API review.

API has been approved in ProxyConfig

**Approvals**

Feature was approved 

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.

Feature was approved in 2019 before TOC approval was required.

---

## Beta

### Requirements: 

**Design**

- [x] Design doc describing the intention of the feature, how it will be
	implemented, and any thoughts on how to test the feature has been approved by
	relevant work group leads

This has been implemented and tested since 2019 (4 years!).

- [x] Feature coverage and test plans written and approved.

This pre-dates this part of the process, but the feature is tested.

**Docs** 

- [x] Documentation on istio.io includes performance expectations; may have caveats. 

YES - documentation lists it may have faster startup.

- [x] Documentation on istio.io includes samples/tutorials. 

N/A - I don't think we need samples here. We just need install steps, which we have.

- [x] Documentation on istio.io includes appropriate glossary entries. 

N/A - we don't introduce any vocabulary here. Users may not understand "distroless", but we link to the docs. This phrase is localized to only a single document and doesn't need to be more broad.

- [x] All new documentation containing user actions includes istio.io tests.

YES/NA - no user actions other than a single `--set values.global.variant=distroless`.

- [x] Release notes have been added. 

YES - when the feature was merged long ago. Once promoted we will note the promotion in the release notes.

- [x] Upgrade notes have been added. 

YES - none needed.

**Tests**

- [x] Integration tests cover feature edge cases

YES - The full Istio integration test suite is ran on each PR.

- [x] End-to-end tests cover samples/tutorials

YES - The full Istio integration test suite is ran on each PR. The only sample/tutorial is the install.

- [x] Fixed issues have tests to prevent regressions
- [x] Stability/stress test suite includes coverage for the feature.

N/A. Its overkill to run 2x suite every time when this is extremely unlikely to have any impact.

**Performance**

- [x] Feature coverage and test plans written and approved 

N/A

- [x] Tests exist with the feature enabled that can be integrated with our automated performance testing.

YES - The full Istio integration test suite is ran on each PR.

**API**

- [x] TOC has reviewed the API and determined it to be complete. 

YES - only a minor API in ProxyConfig which was approved.

**Tooling**

- [x] Any necessary tooling to use/debug the feature has been implemented and is complete. 

YES - we essentially depend on Kubernetes Ephemeral Containers and document how to use it.

**Bugs**

- [ ] Feature has no known major issues.

No: https://github.com/istio/istio/issues/37235. bug-report does not fully support this mode.

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


