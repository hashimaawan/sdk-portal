# V2 Kubernetes Registry Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBSZWdpc3RyeSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesRegistryRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ClusterUuids` | `[]string` | Optional | An array containing the UUIDs of Kubernetes clusters. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2KubernetesRegistryRequest := models.V2KubernetesRegistryRequest{
        ClusterUuids:          []string{
            "bd5f5959-5e1e-4205-a714-a914373942af",
            "50c2f44c-011d-493e-aee5-361a4a0d1844",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



