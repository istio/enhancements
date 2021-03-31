# Feature: Gateway Injection

**Feature name:** Gateway Injection

**Primary lead(s):** @howardjohn

**Short description:** Injecting gateway deployments to enabled minimal configuration and simplified operations.

---

## Experimental

### Requirements:

- [ ] [User stories](insert_your_link_here) reviewed in a work group meeting.

- [x] [RFC Authored] - [Injector V2](https://docs.google.com/document/d/1Rmp9B3DDypgMCau-YAqidx_r3qvKLZj6jUX-t22zj84/).

- [x] [Documentation](https://preliminary.istio.io/latest/docs/setup/additional-setup/sidecar-injection/#custom-templates-experimental) and [here](https://preliminary.istio.io/latest/docs/setup/additional-setup/external-controlplane/) for enabling and using the feature.

- [ ] [Feedback plan](insert_your_link_here). ??

- [x] Disabled by default.

- [x] No impact on performance when the feature is disabled.

---

## Alpha

### Requirements:

**Design**

- [x] RFC has been approved describing the intention of the feature as well as the user stories behind the feature.

**Config**

- [x] Explicit user action is required to enable this feature (e.g. a config field, config resource, or installation action).

> [Documentation](https://preliminary.istio.io/latest/docs/setup/additional-setup/sidecar-injection/#custom-templates-experimental)

**Docs**

- [x] Reference docs are published to preliminary.istio.io or the Istio wiki.
  
There are no reference docs required for this feature.

- [x] Basic feature docs are published on preliminary.istio.io describing what the feature does, how to use it, and any caveats.

> [Documentation](https://preliminary.istio.io/latest/docs/setup/additional-setup/sidecar-injection/#custom-templates-experimental).

- [x] Release notes entries added as appropriate
- [x] Upgrade notes entries added as appropriate

**Tests**

- [x] Automated integration tests cover core use cases with the feature enabled. [Link](https://github.com/istio/istio/blob/73e56211605aaa80de48f9147c94a05701169995/tests/integration/pilot/ingress_test.go#L406)
- [x] When disabled, the feature does not affect system stability or performance. The feature does nothing when not enabled.

**API**

- [x] Initial API review. API approved by environments working group

**Approvals**

- [ ] The appropriate work group(s) have reviewed and approved promotion of the feature.
- [ ] The TOC has reviewed and approved promotion of the feature as part of the
  roadmap for a release.

---

## Beta

### Requirements:

**Design**

- [x] Design doc describing the intention of the feature, how it will be
  implemented, and any thoughts on how to test the feature has been approved by
  relevant work group leads. [Design Doc](https://docs.google.com/document/d/1Rmp9B3DDypgMCau-YAqidx_r3qvKLZj6jUX-t22zj84/).
- [ ] Feature coverage and test plans written and approved.

**Docs**

- [ ] Documentation on istio.io includes performance expectations; may have caveats.
- [x] Documentation on istio.io includes samples/tutorials. [Here](https://preliminary.istio.io/latest/docs/setup/additional-setup/sidecar-injection/#custom-templates-experimental) and [here](https://preliminary.istio.io/latest/docs/setup/additional-setup/external-controlplane/) for enabling and using the feature.
- [x] Documentation on istio.io includes appropriate glossary entries. No glossary entries needed, this uses existing concepts.
- [x] All new documentation containing user actions includes istio.io tests. Yes, the documentation has a test.
- [x] Release notes have been added.
- [x] Upgrade notes have been added.

**Tests**

- [ ] Integration tests cover feature edge cases
- [x] End-to-end tests cover samples/tutorials. Documentation has page tests.
- [x] Fixed issues have tests to prevent regressions. There are no known issues with this feature.
- [ ] Stability/stress test suite includes coverage for the feature.

**Performance**

- [ ] Feature coverage and test plans written and approved
- [ ] Tests exist with the feature enabled that can be integrated with our automated performance testing.

**API**

- [ ] TOC has reviewed the API and determined it to be complete.

**Tooling**

- [x] Any necessary tooling to use/debug the feature has been implemented and is complete. Injection is an existing mechanism with established tooling.

**Bugs**

- [x] Feature has no known major issues.

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


