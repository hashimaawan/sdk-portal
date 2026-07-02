# V2 Kubernetes Clusters Clusterlint Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2KubernetesClustersClusterlintRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ExcludeChecks` | `[]string` | Optional | An array of checks that will be run when clusterlint executes checks. |
| `ExcludeGroups` | `[]string` | Optional | An array of check groups that will be omitted when clusterlint executes checks. |
| `IncludeChecks` | `[]string` | Optional | An array of checks that will be run when clusterlint executes checks. |
| `IncludeGroups` | `[]string` | Optional | An array of check groups that will be run when clusterlint executes checks. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2KubernetesClustersClusterlintRequest := models.V2KubernetesClustersClusterlintRequest{
        ExcludeChecks:         []string{
            "default-namespace",
        },
        ExcludeGroups:         []string{
            "workload-health",
        },
        IncludeChecks:         []string{
            "bare-pods",
            "resource-requirements",
        },
        IncludeGroups:         []string{
            "basic",
            "doks",
            "security",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



