# Service Components that Are Part of This Deployment

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZpY2UlMjUyMGNvbXBvbmVudHMlMjUyMHRoYXQlMjUyMGFyZSUyNTIwcGFydCUyNTIwb2YlMjUyMHRoaXMlMjUyMGRlcGxveW1lbnQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`ServiceComponentsThatArePartOfThisDeployment`


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
    serviceComponentsThatArePartOfThisDeployment := models.ServiceComponentsThatArePartOfThisDeployment{
        Name:                  models.ToPointer("web"),
        SourceCommitHash:      models.ToPointer("54d4a727f457231062439895000d45437c7bb405"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



