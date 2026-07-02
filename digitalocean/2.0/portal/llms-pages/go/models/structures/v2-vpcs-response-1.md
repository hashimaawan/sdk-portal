# V2 Vpcs Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBWcGNzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2VpcsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Vpc` | [`*models.Vpc`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/vpc.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2VpcsResponse1 := models.V2VpcsResponse1{
        Vpc:                   models.ToPointer(models.Vpc{
            Description:           models.ToPointer("description8"),
            Name:                  models.ToPointer("name2"),
            IpRange:               models.ToPointer("ip_range4"),
            Region:                models.ToPointer("region8"),
            Default:               models.ToPointer(false),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



