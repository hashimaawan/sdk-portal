# Kubernetes Cluster User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVyVXNlcg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`KubernetesClusterUser`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Groups` | `[]string` | Optional | A list of in-cluster groups that the user belongs to. |
| `Username` | `*string` | Optional | The username for the cluster admin user. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    kubernetesClusterUser := models.KubernetesClusterUser{
        Groups:                []string{
            "k8saas:authenticated",
        },
        Username:              models.ToPointer("sammy@digitalocean.com"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



