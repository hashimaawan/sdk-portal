# Reserved Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc2VydmVkSXA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`ReservedIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Droplet` | [`*models.ReservedIpDroplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/reserved-ip-droplet.md) | Optional | This is a container for any-of cases. |
| `Ip` | `*string` | Optional | The public IP address of the reserved IP. It also serves as its identifier. |
| `Locked` | `*bool` | Optional | A boolean value indicating whether or not the reserved IP has pending actions preventing new ones from being submitted. |
| `ProjectId` | `*uuid.UUID` | Optional | The UUID of the project to which the reserved IP currently belongs. |
| `Region` | [`*models.Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/region.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    reservedIp := models.ReservedIp{
        Droplet:               models.ToPointer(models.ReservedIpDropletContainer.FromObject(interface{}("[key1, val1][key2, val2]"))),
        Ip:                    models.ToPointer("45.55.96.47"),
        Locked:                models.ToPointer(true),
        ProjectId:             models.ToPointer(uuid.MustParse("746c6152-2fa2-11ed-92d3-27aaa54e4988")),
        Region:                models.ToPointer(models.Region{
            Available:             false,
            Features:              []string{
                "features7",
                "features8",
                "features9",
            },
            Name:                  "name6",
            Sizes:                 []string{
                "sizes6",
            },
            Slug:                  "slug0",
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



