[//]: # (The syntax preceeding this line is a comment marker used to help guide the author in populating this document)
[//]: # (to github. Unlike HTML comments commonly used throughout istio.io documentation, this comment will not be rendered)
[//]: # (by github. Comments must be separated by carriage return preceding and concluding the text and be a single line.)

[//]: # (This is a living document representing the maturity of a feature. Completion of this template enables Istio work groups)
[//]: # (to collect information on potential new functionality. This template should be completed before users are exposed to)
[//]: # (any new experimental feature. Please complete this template during development.)

[//]: # (The feature implementation section must be completed before submission of the document.)

# Feature:

[//]: # (All information in this section is mandatory.)

**Feature name:** Automatic Mutual TLS

[//]: # (The name of the feature, e.g. Multiple control planes)

**Primary lead(s):** @incfly

[//]: # (The primary lead or leads responsible for the feature. These individuals serve as a point of contact for the feature.)

**Short description:**

[//]: # (A short description of the feature. One or two sentences maximum.)


**Design Docs:**

[//]: # (Design docs for feature)

* https://docs.google.com/document/d/1yEMDRO2FZCyZnDK1AzNmjQtbtQqE7wN8YoM65FAH7uA/edit?skip_itp2_check=true&pli=1#heading=h.7df973t639nj

**Relevant Documentation:**

[//]: # (Links to relevant documentation for feature)
* istio.io/latest/docs/tasks/security/authentication/authn-policy/#auto-mutual-tls
* 
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

- [X] [RFC](https://docs.google.com/document/d/1yEMDRO2FZCyZnDK1AzNmjQtbtQqE7wN8YoM65FAH7uA/edit) has been approved describing the intention of the feature as well as the user stories behind the feature. 

**Config**

- [X] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action). `enableAutoMtls` in [MeshConfig](https://istio.io/latest/docs/reference/config/istio.mesh.v1alpha1/)

**Docs**

- [X] [Reference docs](https://istio.io/latest/docs/tasks/security/authentication/authn-policy/#auto-mutual-tls) are published to preliminary.istio.io or the Istio wiki.
- [X] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats. Same as above.
- [X] [Release notes](https://istio.io/latest/news/releases/1.4.x/announcing-1.4/#automatic-mutual-tls) entries added as appropriate
- [X] Upgrade notes entries added as appropriate. N/A

**Tests**

- [X] [Automated integration](https://github.com/istio/istio/blob/e68b6b629d64277943e736ad7c6104ff1dd295a3/tests/integration/security/reachability_test.go#L114) tests cover core use cases with the feature enabled. 
- [X] When disabled, the feature does not affect system stability or performance. 

**API**

- [X] Initial API review. `enableAutomaticMTLS` Existing in MeshConfig since 1.4.

**Approvals**

- [X] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [X] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.

---

## Beta

### Requirements: 

**Design**

- [x] Design doc describing the intention of the feature, how it will be
	implemented, and any thoughts on how to test the feature has been approved by
	relevant work group leads
- [x] Feature coverage and test plans written and approved.

**Docs** 

- [x] Documentation on istio.io includes performance expectations; may have caveats. 
 Same as above, mTLS vs Plaintext performance comparison.
- [x] Documentation on istio.io includes samples/tutorials. 
istio.io/latest/docs/tasks/security/authentication/authn-policy/#auto-mutual-tls
- [X] Documentation on istio.io includes appropriate [glossary entries](https://preliminary.istio.io/latest/docs/reference/glossary/#auto-mtls).
- [x] All new documentation containing user actions includes istio.io tests.
- [x] Release notes have been added. On By Default Since 1.5, Not Applied
- [x] Upgrade notes have been added. N/A.

**Tests**

- [X] Integration tests cover feature edge cases, [headless service](https://github.com/istio/istio/blob/e68b6b629d64277943e736ad7c6104ff1dd295a3/tests/integration/security/reachability_test.go#L162)
- [X] End-to-end tests cover samples/tutorials. N/A existing feature post requirement.
- [X] Fixed issues have tests to prevent regressions. N/A.
- [X] Stability/stress [test](https://github.com/istio/tools/tree/master/perf/load/auto-mtls) suite includes coverage for the feature.

**Performance**

- [x] Feature coverage and test plans written and approved 

[Test Plan Section](https://docs.google.com/document/d/1yEMDRO2FZCyZnDK1AzNmjQtbtQqE7wN8YoM65FAH7uA/edit#heading=h.7df973t639nj)

- [X] [Tests exist](https://github.com/istio/tools/tree/master/perf/benchmark/configs/istio/plaintext) with the feature enabled that can be integrated with our automated performance testing.

**API**

- [x] TOC has reviewed the API and determined it to be complete. 

**Tooling**

- [ ] Any necessary tooling to use/debug the feature has been implemented and is complete. 

**Bugs**

- [X] Feature has no known major issues.

**Approvals**

- [X] The appropriate work group(s) have reviewed and approved promotion of the [feature](https://docs.google.com/document/d/1cU4TFqYdir1luUN4gf3mTvujb4LugNLhcNffOluQyns/edit?disco=AAAALq26fXg&ts=60467f2f&usp_dm=true&resourcekey=0-tIc8kq3LHGokG4FHfXJ5CQ).
- [ ] The supportability review panel has reviewed promotion of the feature. TODO: WIP.  
- [X] The TOC has reviewed and approved promotion of the feature as part of the
	road map for a release.

---

## Stable

### Requirements: 

**Performance**

- [x] Latency, throughput, and scalability are quantified and documented on
	istio.io. 

istio.io/latest/blog/2020/large-scale-security-policy-performance-tests/#data

**Bugs**

- [x] Feature has no known major issues. 

**Approvals**

- [X] The appropriate work group(s) have reviewed and approved promotion of the [feature](https://docs.google.com/document/d/1cU4TFqYdir1luUN4gf3mTvujb4LugNLhcNffOluQyns/edit?disco=AAAALq26fXg&ts=60467f2f&usp_dm=true&resourcekey=0-tIc8kq3LHGokG4FHfXJ5CQ).
- [ ] The supportability review panel has reviewed promotion of the feature.  
- [X] The TOC has reviewed and approved promotion of the feature as part of the
	roadmap for a release.


