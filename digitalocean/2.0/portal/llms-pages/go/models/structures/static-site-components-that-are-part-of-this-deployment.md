# Static Site Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXRpYyUyNTIwU2l0ZSUyNTIwY29tcG9uZW50cyUyNTIwdGhhdCUyNTIwYXJlJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhpcyUyNTIwZGVwbG95bWVudA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`StaticSiteComponentsThatArePartOfThisDeployment`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `*string` | Optional | - |
| `SourceCommitHash` | `*string` | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    staticSiteComponentsThatArePartOfThisDeployment := models.StaticSiteComponentsThatArePartOfThisDeployment{
        Name:                  models.ToPointer("web"),
        SourceCommitHash:      models.ToPointer("54d4a727f457231062439895000d45437c7bb405"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



