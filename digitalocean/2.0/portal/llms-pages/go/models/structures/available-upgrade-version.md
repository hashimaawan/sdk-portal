# Available Upgrade Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkF2YWlsYWJsZVVwZ3JhZGVWZXJzaW9u

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`AvailableUpgradeVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `KubernetesVersion` | `*string` | Optional | The upstream version string for the version of Kubernetes provided by a given slug. |
| `Slug` | `*string` | Optional | The slug identifier for an available version of Kubernetes for use when creating or updating a cluster. The string contains both the upstream version of Kubernetes as well as the DigitalOcean revision. |
| `SupportedFeatures` | `[]string` | Optional | The features available with the version of Kubernetes provided by a given slug. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    availableUpgradeVersion := models.AvailableUpgradeVersion{
        KubernetesVersion:     models.ToPointer("1.16.13"),
        Slug:                  models.ToPointer("1.16.13-do.0"),
        SupportedFeatures:     []string{
            "cluster-autoscaler",
            "docr-integration",
            "token-authentication",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



