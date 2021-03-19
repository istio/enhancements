# Feature Maturity

Maturity of features in Istio indicate to users what they can [expect](https://istio.io/latest/about/feature-stages/) by using these
features. In Istio, we track these requirements using a [template](features/feature_template.md). Once all
requirements for promoting a feature to the next level are met, the [features](features.yaml)
file may be updated to indicate this maturity level.

## Features.yaml

Features.yaml tracks the maturity of all Istio features. This is written
in YAML so that it can be easily processed by any tooling that needs to
track feature maturity. Each feature in Istio should have a features
entry as described below.

```
features:
  - name: "Protocols:HTTP1.1/HTTP2/gRPC/TCP"
    level
      - checkList: 
        current:
        promotionBefore:
    state
      - state:
        begin:
        details:
```

* **Name** indicates the name of the feature.
* **level** indicates the maturity level of a feature.
* **level.checklist** is the path to the checklist to track a feature's maturity.
* **level.current** is the current maturity level of the feature. This can be `experimental`, `alpha`, `beta`, or `stable`. Experimental is an optional maturity level that can be skipped. For alpha, beta, and stable, all requirements for the previous levels must be met before a feature can meet the next level (i.e. a stable feature has met the requirements of both alpha and beta). There may be features for which a requirement is not applicable.
* **level.promotionBefore** indicates the Istio release by which the next promotion of a feature is expected. Up until a feature is stable, a feature is expected to be continously maturing. The `promotionBefore` field indicates when a feature is expected to reach the next level of maturity. If a feature doesn't get promoted within that timespan, a decision needs to be made as to whether that promotion date should be extended or that feature should be deprecated. A long window is given with the assumption that it should be enough time for features to be promoted, so the default is to deprecate that feature after this date. However, exceptions may be made to this in a feature by feature basis. In some rare circumstances, features will be permanently in a state below stable and never expected to be promoted. For those circumstances, this field can be marked `never`.
* **state** indicates the current state of a feature. This can be `active`,`deprecated`, or `retired`. Active features are safe to use according to the [feature phase definitions](https://istio.io/latest/about/feature-stages/). When a feature is deprecated, both the deprecated feature and any replacement are supported but users should move off of the deprecated feature as it will be removed in a future release. Retired features are no longer supported and should not be used. Deprecation time varies depending on the [current maturity level](https://istio.io/latest/about/feature-stages/).
* **state.details** should be set when a feature moves out of the active state. These do not apply to active features.
* **state.begin** indicates the date at which the feature will move to the next state. For deprecated features, this is the date that the feature will be retired. 
