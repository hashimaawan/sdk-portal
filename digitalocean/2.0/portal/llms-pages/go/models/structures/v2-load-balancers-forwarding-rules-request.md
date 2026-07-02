# V2 Load Balancers Forwarding Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMEZvcndhcmRpbmclMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2LoadBalancersForwardingRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ForwardingRules` | [`[]models.ForwardingRule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/forwarding-rule.md) | Required | **Constraints**: *Minimum Items*: `1` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2LoadBalancersForwardingRulesRequest := models.V2LoadBalancersForwardingRulesRequest{
        ForwardingRules:       []models.ForwardingRule{
            models.ForwardingRule{
                CertificateId:         models.ToPointer("892071a0-bb95-49bc-8021-3afd67a210bf"),
                EntryPort:             443,
                EntryProtocol:         models.EntryProtocol_Https,
                TargetPort:            80,
                TargetProtocol:        models.TargetProtocol_Http,
                TlsPassthrough:        models.ToPointer(false),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



