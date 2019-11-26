# Enhancement Tracking and Backlog
Enhancement Tracking and Backlog Repo for Istio Releases. Owned by TOC.

This repo contains issues and Istio enhancement proposal. These issues are umbrellas for new enhancements to be added to Istio. An enhancement usually takes multiple releases to complete. And an enhancement can be tracked as backlog items before work begins. An enhancement may be filed once there is consensus in at least one Istio working group.

## Is My Thing an Enhancement?

We are trying to figure out the exact shape of an enhancement. Until then here are a few rough heuristics.

An enhancement is anything that:

- a blog post would be written about after its release (ex. [v1beta1 authorization policy](https://istio.io/blog/2019/v1beta1-authorization-policy/))
- requires multiple parties/SIGs/owners participating to complete (ex. auto mTLS)
- will be graduating from one stage to another (ex. alpha to beta, beta to GA)
- needs significant effort or changes Istio in a significant way (ex. something that would take 10 person-weeks to implement, introduce or redesign a system component, or introduces API changes)
- impacts the UX or operation of Istio substantially such that engineers using Istio will need retraining
- users will notice and come to rely on

It is unlikely an enhancement if it is:
- fixing a flaky test
- refactoring code
- performance improvements, which are only visible to users as faster API operations, or faster control loops
- adding error messages or events

If you are not sure, ask someone in the working group where you initially circulated the idea.

## When to Create a New Enhancement Issue

Create an issue here once you:
- have circulated your idea to see if there is interest
   - through Community Meetings, working group meetings, discuss.istio.io lists, or an issue in github.com/istio/istio
- (optionally) have done a prototype in your own fork
- have identified people who agree to work on the enhancement
  - many enhancements will take several releases to progress through Alpha, Beta, and Stable stages
  - you and your team should be prepared to work on the approx. 9mo - 1 year that it takes to progress to Stable status
- are ready to be the project-manager for the enhancement

## Why are Enhancements Tracked

Once users adopt an enhancement, they expect to use it for an extended period of time. Therefore, we hold new enhancements to a
high standard of conceptual integrity and require consistency with other parts of the system, thorough testing, and complete
documentation. As the project grows no single person can track whether all those requirements are met. The development
of an enhancement often spans three stages: Alpha, Beta, and Stable; Enhancement Tracking Issues provide a
checklist that allows for different approvers for different aspects, and ensures that nothing is forgotten across the
development lifetime of an enhancement.

## When to Comment on an Enhancement Issue

Please comment on the enhancement issue to:
- request a review or clarification on the process
- update status of the enhancement effort
- link to relevant issues in other repos

Please do not comment on the enhancement issue to:
- discuss a detail of the design, code or docs. Use a linked-to-issue or PR for that
