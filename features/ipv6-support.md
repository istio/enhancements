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

IPv6 support for Kubernetes

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):**

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:**
Add support for IPv6 network model in Istio. With this, Istio now supports both IPv6 and IPv4 network model but not dual-stack at the moment.

[//]: # (A short description of the feature. One or two sentences maximum.)


**Design Docs:**

[//]: # (Design docs for feature)


**Relevant Documentation:**
[Add IPv6 support](https://github.com/istio/istio/issues/1756)

[//]: # (Links to relevant documentation for feature)

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


[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [ ] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature
---

## Alpha

### Requirements: 

**Design**

- [ ] RFC has been approved describing the intention of the feature as well as the user stories behind the feature. 
N/A

**Config**

- [ ] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). 

> Link to instructions for enabling

**Docs**

- [ ] Reference docs are published to preliminary.istio.io or the Istio wiki.
- [ ] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. 
- [ ] Release notes entries added as appropriate
- [ ] Upgrade notes entries added as appropriate

**Tests**

- [x] Automated integration tests cover core use cases with the feature enabled. 
- [X] When disabled, the feature does not affect system stability or performance. 

**API**

- [ ] Initial API review.
N/A

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [x] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.

**Promotion**

[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [x] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature

---

## Beta

### Requirements: 

- Overall Beta status tracker: https://github.com/istio/istio/issues/60425

**Design**

- [x] Design doc describing the intention of the feature, how it will be
	implemented, and any thoughts on how to test the feature has been approved by
	relevant work group leads
	- IPv6 design/problem-statement doc by @zhlsunshine (EPA subgroup): https://docs.google.com/document/d/1cPXR9Kdn7aILzQ1FO9AmCTz3K2OyvVGtS4J5FQUBaf8/edit?tab=t.0#heading=h.crqgw0rmjf9m
	- Dual-stack design doc: https://docs.google.com/document/d/15LP2XHpQ71ODkjCVItGacPgzcn19fsVhyE7ruMGXDyU/edit?usp=sharing
	- Dual-stack RFC: https://docs.google.com/document/d/1oT6pmRhOw7AtsldU0-HbfA0zA26j9LYiBD_eepeErsQ/edit?usp=sharing
	- The IPv6 RFC identified the foundational problems; the dual-stack design and RFC represent the complete, implemented solution. Since dual-stack (which fully encompasses IPv6) is already at Beta, the design requirements for IPv6 Beta promotion are satisfied.
- [x] Feature coverage and test plans written and approved.
	- Coverage is tracked in the Beta status issue: https://github.com/istio/istio/issues/60425

**Docs** 

- [x] Documentation on istio.io includes performance expectations; may have caveats. 
	- Caveats and prerequisites for IPv6/dual-stack environments: https://istio.io/latest/docs/ops/deployment/platform-requirements/
- [x] Documentation on istio.io includes samples/tutorials.
	- IPv6 sample: https://github.com/istio/istio/blob/master/samples/tcp-echo/tcp-echo-ipv6.yaml
	- Dual-stack samples are available under https://github.com/istio/istio/tree/master/samples
- [ ] Documentation on istio.io includes appropriate glossary entries. 
- [x] All new documentation containing user actions includes istio.io tests.
	- Dual-stack docs test exists: https://prow.istio.io/view/gs/istio-prow/pr-logs/pull/istio_istio.io/17344/doc.test.dualstack_istio.io/2048079445612302336
	- IPv6 docs test job added in test-infra: https://github.com/istio/test-infra/pull/5936 (`doc.test.ipv6.profile-default`, optional presubmit trigger via `/test doc.test.ipv6.profile-default`)
	- IPv6 docs test fixes in istio.io: https://github.com/istio/istio.io/pull/17424
- [ ] Release notes have been added. Planned after TOC approval of this PR and final confirmation of Beta promotion.
- [ ] Upgrade notes have been added. 

**Tests**

- [x] Integration tests cover feature edge cases
	- IPv6 postsubmit integration job: https://prow.istio.io/?job=integ-ambient-ipv6_istio_postsubmit
	- IPv6 postsubmit integration job (release-1.28): https://prow.istio.io/?job=integ-ambient-ipv6_istio_release-1.28_postsubmit
	- IPv6 postsubmit integration job (core): https://prow.istio.io/?job=integ-ipv6_istio_postsubmit
	- IPv6 presubmit integration job exists (ambient-ipv6 variant).
	- IPv6 presubmit integration job exists (regular ipv6 variant).
	- IPv6 docs integration job added in test-infra: https://github.com/istio/test-infra/pull/5936
	- IPv6 docs integration fixes merged in istio.io: https://github.com/istio/istio.io/pull/17424
- [x] End-to-end tests cover samples/tutorials
	- IPv6 docs test coverage added via https://github.com/istio/test-infra/pull/5936
	- Follow-up fixes merged via https://github.com/istio/istio.io/pull/17424 to make docs tests pass on IPv6-only kind
- [x] Fixed issues have tests to prevent regressions
		- https://github.com/istio/istio/issues/54267 fixed by https://github.com/istio/istio/pull/54269 — added `TestReadToJSONIPv4` + `TestReadToJSONIPv6` unit tests in `pkg/envoy/proxy_test.go`
		- https://github.com/istio/istio/issues/56587 fixed by https://github.com/istio/istio/pull/56626 — added unit test in `tools/istio-iptables/pkg/capture/run_linux_test.go`
		- https://github.com/istio/istio/pull/51221 — includes iptables test updates with IPv6 SNAT golden files in `cni/pkg/iptables/iptables_test.go`
- [x] Stability/stress test suite includes coverage for the feature.
	- N/A for this promotion: IPv6 Beta promotion relies on existing integration, docs, and performance coverage; no separate IPv6-specific stress suite is required.

**Performance**

- [x] Feature coverage and test plans written and approved 
	- Performance test scripts can be run on either IPv6-only or IPv4 clusters.
	- Performance benchmark scripts and usage: https://github.com/istio/tools/blob/master/perf/benchmark/README.md
- [x] Tests exist with the feature enabled that can be integrated with our automated performance testing.
	- Existing performance scripts are reusable for IPv6 and IPv4 environments.

**API**

- [x] TOC has reviewed the API and determined it to be complete. 
	- API examples supporting both IPv4 and IPv6:
	  - Sidecar API (`networking/v1alpha3/sidecar.proto`) documents listener bind IP as IPv4 or IPv6.
	  - VirtualService API (`networking/v1alpha3/virtual_service.proto`) documents source/destination subnet matching as IPv4 or IPv6.
	  - Ambient mode example: IPv6-related ambient fixes are tracked in https://github.com/istio/istio/pull/59083.
	- Default expectation for newly added APIs is dual-family behavior (IPv4 and IPv6) wherever IP address fields are used.

**Tooling**

- [x] Any necessary tooling to use/debug the feature has been implemented and is complete. 
	- There is no dedicated IPv6-only `istioctl` debug command; standard `istioctl` debug workflows are used for both IPv4 and IPv6.
	- `istioctl x workload configure` supports IPv6 via `--ingressIP`: https://github.com/istio/istio/blob/master/releasenotes/notes/45407.yaml
	- **Platform prerequisite**: `istioctl proxy-config` / `istioctl dashboard` require containerd ≥ 1.5.0 on IPv6 clusters (earlier versions had broken IPv6 port-forwarding). Reference: https://github.com/istio/istio/issues/34358, https://github.com/istio/istio/issues/35177

**Bugs**

- [x] Feature has no known major issues.
	- Reported post-Alpha IPv6 issues have been fixed. Proof links:
	  - https://github.com/istio/istio/issues/34966
	  - https://github.com/istio/istio/issues/35915
	  - https://github.com/istio/istio/issues/36961
	  - https://github.com/istio/istio/issues/46625
	  - https://github.com/istio/istio/issues/47412
	  - https://github.com/istio/istio/issues/49476
	  - https://github.com/istio/istio/issues/50162
	  - https://github.com/istio/istio/pull/51221
	  - https://github.com/istio/istio/issues/54267
	  - https://github.com/istio/istio/issues/56587
	  - https://github.com/istio/istio/issues/58249

**Approvals**

- [x] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The supportability review panel has reviewed promotion of the feature.  
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

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The [supportability review panel](https://docs.google.com/document/d/1w0epyFhhDSf_TwFEfa_lrn1v61mXNJKpEp_kUgp4sSc/edit#) has reviewed the feature in order to find any supportability concerns.  
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.


**Promotion**

[//]: # (Once all other items are completed, features.yaml should be updated to promote the feature)

- [ ] [features.yaml](https://github.com/istio/enhancements/blob/master/features.yaml) updated for this feature
