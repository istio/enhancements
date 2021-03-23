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

**Short description:**

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

### Requirements:

[//]: # (All information in this section is mandatory for promotion. Please modify the links in this)
[//]: # (section.)

- [ ] [User stories](insert_your_link_here) reviewed in a work group meeting.

[//]: # (User stories are a way to communicate user value. User stories follow the style)
[//]: # (as a [type of user], I want [an action] so that [a benefit/a value]. Istio currently has no user)
[//]: # (story template. Maybe you can make one?)

[//]: # (User stories must be presented in a work group meeting. They need no approval and are later integrated)
[//]: # (into the RFCs, which do need approval for alpha. You may find value to negotiate within the work group where the)
[//]: # (user stories are presented to help clarify the user stories.)

- [ ] [RFC Authored] - [create an RFC using template](https://docs.google.com/document/d/1ewJoCcw5-04crH-M0xw4zFxz1cfwVCPnNyW4K3m4Yyc/template/preview).

[//]: # (An RFC is mandatory to graduate to experimental. The RFC does not have to be reviewed in a work group)
[//]: # (meeting to graduate to experimental.)

- [ ] [Documentation](insert_your_link_here) for enabling and using the feature.

[//]: # (The documentation instructions may exist on the developer wiki or the team drive. They may include instructions)
[//]: # (for building running a `istioctl experimental command`, or using the preview profile,)
[//]: # (or any other relevant information.)

- [ ] [Feedback plan](insert_your_link_here).

[//]: # (This may include user feedback meetings, discuss.istio.io conversations, GitHub issues, or mailing lists.)

- [ ] Disabled by default.

- [ ] No impact on performance when the feature is disabled.

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

implemented, and any thoughts on how to test the feature has been approved by
relevant work group leads

- [ ] Feature coverage and test plans written and approved.

**Docs** 

- [x] Documentation on istio.io includes performance expectations; may have caveats. 

YES - documentation lists it may have faster startup.

- [x] Documentation on istio.io includes samples/tutorials. 

N/A - I don't think we need samples here. We just need install steps, which we have

- [x] Documentation on istio.io includes appropriate glossary entries. 

N/A - we don't introduce any vocabulary here. Users may not understand "distroless", but we link to the docs. This phrase is localized to only a single document and doesn't need to be more broad.

- [x] All new documentation containing user actions includes istio.io tests.

YES/NA - no user actions other than a single `--set tag=1.9.0-distroless`

- [x] Release notes have been added. 

YES - when the feature was merged long ago

- [x] Upgrade notes have been added. 

YES - none needed

**Tests**

- [ ] Integration tests cover feature edge cases

NO - we only cover basic integration test. We may have gaps in things that depend on internal tools, like istioctl. Probably not, but its not tested.

- [x] End-to-end tests cover samples/tutorials

YES - e2e tests cover the full install

- [x] Fixed issues have tests to prevent regressions
- [ ] Stability/stress test suite includes coverage for the feature.
NO. Its highly likely overkill to run 2x suite every time when this is extremely unlikely to have any impact. We can likely run it one-off?

**Performance**

- [x] Feature coverage and test plans written and approved 

N/A

- [x] Tests exist with the feature enabled that can be integrated with our automated performance testing.

**API**

- [ ] TOC has reviewed the API and determined it to be complete. 

Like NA, as there is no API, unless we consider the docker tag name an API. Will leave to TOC to decide.

**Tooling**

- [ ] Any necessary tooling to use/debug the feature has been implemented and is complete. 

NO - we essentially depend on Kubernetes Ephemeral Containers to be in widespread use in order to facilitate debugging of the proxy or control plane once distroless images are in use. This is apparently beta in Kubernetes 1.21.

**Bugs**

- [ ] Feature has no known major issues.

No: https://github.com/istio/istio/issues?q=is%3Aissue+distroless+is%3Aopen+sort%3Aupdated-desc

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


