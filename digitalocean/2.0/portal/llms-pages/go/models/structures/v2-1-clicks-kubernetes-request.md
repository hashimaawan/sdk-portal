# V2 1 Clicks Kubernetes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjAxJTI1MjBDbGlja3MlMjUyMEt1YmVybmV0ZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V21ClicksKubernetesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AddonSlugs` | `[]string` | Required | An array of 1-Click Application slugs to be installed to the Kubernetes cluster. |
| `ClusterUuid` | `string` | Required | A unique ID for the Kubernetes cluster to which the 1-Click Applications will be installed. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v21ClicksKubernetesRequest := models.V21ClicksKubernetesRequest{
        AddonSlugs:            []string{
            "kube-state-metrics",
            "loki",
        },
        ClusterUuid:           "50a994b6-c303-438f-9495-7e896cfe6b08",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



