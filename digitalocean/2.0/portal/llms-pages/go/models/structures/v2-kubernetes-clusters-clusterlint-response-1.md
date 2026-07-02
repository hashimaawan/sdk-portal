# V2 Kubernetes Clusters Clusterlint Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `RunId` | `*string` | Optional | ID of the clusterlint run that can be used later to fetch the diagnostics. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2KubernetesClustersClusterlintResponse1 := models.V2KubernetesClustersClusterlintResponse1{
        RunId:                 models.ToPointer("50c2f44c-011d-493e-aee5-361a4a0d1844"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



