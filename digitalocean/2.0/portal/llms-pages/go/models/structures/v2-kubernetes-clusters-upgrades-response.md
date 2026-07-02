# V2 Kubernetes Clusters Upgrades Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXBncmFkZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesClustersUpgradesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AvailableUpgradeVersions` | [`models.Optional[[]models.AvailableUpgradeVersion]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/available-upgrade-version.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2KubernetesClustersUpgradesResponse := models.V2KubernetesClustersUpgradesResponse{
        AvailableUpgradeVersions: models.NewOptional(models.ToPointer([]models.AvailableUpgradeVersion{
            models.AvailableUpgradeVersion{
                KubernetesVersion:     models.ToPointer("kubernetes_version0"),
                Slug:                  models.ToPointer("slug2"),
                SupportedFeatures:     []string{
                    "supported_features3",
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        })),
        AdditionalProperties:     map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



