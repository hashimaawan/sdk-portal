# V2 Reserved Ips Actions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ReservedIpsActionsRequest`


# Inherits From

[`BaseType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/base-type.md)


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DropletId` | `int` | Required | The ID of the Droplet that the reserved IP will be assigned to. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2ReservedIpsActionsRequest := models.V2ReservedIpsActionsRequest{
        BaseType:  models.BaseType{
            Type:                  models.ToPointer("V2 Reserved Ips Actions Request"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        DropletId: 758604968,
    }

}
```

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`BaseType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | `*string` | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    baseType := models.BaseTypeInterface(&models.BaseType{
        Type:                  models.ToPointer("BaseType"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    })

}
```



