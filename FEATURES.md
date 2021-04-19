# Feature Maturity

Maturity of features in Istio indicate to users what they can [expect](https://istio.io/latest/about/feature-stages/) by using these
features. In Istio, we track these requirements using a [template](features/feature_template.md). Once all
requirements for the next level are met, [features.yaml](features.yaml) can be updated in order to promote the feature.

## Features.yaml

Features.yaml tracks the maturity of all Istio features. This is written
in YAML so that it can be easily processed by any tooling that needs to
track feature maturity. Each feature in Istio should have a features
entry as described below.

```
features:
- name: "Stackdriver Integration"
    link: "/docs/reference/config/proxy_extensions/stackdriver/"
    level:
      checklist: ""
      maturity: Stable
      nextExpectedPromotion: ""
    deprecation:
      state: "deprecated"
      details:
        replacement: "SelfDrivingStack integration"
        next: "1.10"
    area:  Observability
```

* **name** indicates the name of the feature.
* **area** indicates the area of the feature.
* **link** indicates a primary link that users can navigate to in order to find out more about a feature. This link may be provided to users by tooling consuming features.yaml.
* **level** indicates the maturity level of a feature.
* **level.checklist** is the path to the checklist to track a feature's maturity.
* **level.maturity** is the current maturity level of the feature. This can be `experimental`, `alpha`, `beta`, or `stable`. Experimental is an optional maturity level that can be skipped. For alpha, beta, and stable, all requirements for the previous levels must be met before a feature can meet the next level (i.e. a stable feature has met the requirements of both alpha and beta). There may be features for which a requirement is not applicable.
* **level.nextExpectedPromotion** indicates the Istio release by which the next promotion of a feature is expected. Up until a feature is stable, a feature is expected to continuously mature. If a feature doesn't get promoted, this should be extended or the feature should be deprecated.  In some rare circumstances, features will be permanently in a state below stable and never expected to be promoted. For those circumstances, this field can be marked `never`.
* **deprecation** describes details of deprecated features. 
* **deprecation.state** This can be `deprecated` or `retired`. When a feature is deprecated, users should consider migrating to a replacement as retired features may be removed. Deprecation time varies depending on the [current maturity level](https://istio.io/latest/about/feature-stages/).
* **deprecation.details** should be set when a feature moves out of the active state.
* **deprecation.details.replacement** should specify the checklist(s) for any
	feature replacing this deprecated feature. 
* **deprecation.next** indicates the release in which the feature will be retired. 
