# V2 Domains Records Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DomainsRecordsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DomainRecord` | [`*models.DomainRecord`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/domain-record.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DomainsRecordsResponse1 := models.V2DomainsRecordsResponse1{
        DomainRecord:          models.ToPointer(models.DomainRecord{
            Data:                  models.ToPointer("162.10.66.0"),
            Flags:                 models.NewOptional[int](nil),
            Id:                    models.ToPointer(28448433),
            Name:                  models.ToPointer("www"),
            Port:                  models.NewOptional[int](nil),
            Priority:              models.NewOptional[int](nil),
            Tag:                   models.NewOptional[string](nil),
            Ttl:                   models.ToPointer(1800),
            Type:                  "A",
            Weight:                models.NewOptional[int](nil),
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



