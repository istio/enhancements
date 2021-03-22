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
    level:
      - checkList: 
        maturity:
        nextExpectedPromotion:
	deprecation:
      - state:
        begin:
        details:
		- replacement: 
```

* **Name** indicates the name of the feature.
* **level** indicates the maturity level of a feature.
* **level.checklist** is the path to the checklist to track a feature's maturity.
* **level.maturity** is the current maturity level of the feature. This can be `experimental`, `alpha`, `beta`, or `stable`. Experimental is an optional maturity level that can be skipped. For alpha, beta, and stable, all requirements for the previous levels must be met before a feature can meet the next level (i.e. a stable feature has met the requirements of both alpha and beta). There may be features for which a requirement is not applicable.
* **level.nextExpectedPromotion** indicates the Istio release by which the next promotion of a feature is expected. Up until a feature is stable, a feature is expected to continuously mature. If a feature doesn't get promoted, this should be extended or the feature should be deprecated.  In some rare circumstances, features will be permanently in a state below stable and never expected to be promoted. For those circumstances, this field can be marked `never`.
* **deprecation** indicates the current  deprecation state of a feature. This can be `dprecated`, or `retired`. When a feature is deprecated, users should consider migrating to a replacement as retired features may be removed. Deprecation time varies depending on the [current maturity level](https://istio.io/latest/about/feature-stages/).
* **deprecation.details** should be set when a feature moves out of the active state.
* **deprecation.details.replacement** should specify the checklist(s) for any
	feature replacing this deprecated feature. 
* **deprecation.next** indicates the release in which the feature will be retired. 
