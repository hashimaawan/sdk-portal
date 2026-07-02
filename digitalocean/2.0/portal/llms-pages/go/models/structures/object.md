# Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk9iamVjdA

Metadata about the Kubernetes API object the diagnostic is reported on.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Object`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Kind` | `*string` | Optional | The kind of Kubernetes API object |
| `Name` | `*string` | Optional | Name of the object |
| `Namespace` | `*string` | Optional | The namespace the object resides in the cluster. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    object := models.Object{
        Kind:                  models.ToPointer("config map"),
        Name:                  models.ToPointer("foo"),
        Namespace:             models.ToPointer("kube-system"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



