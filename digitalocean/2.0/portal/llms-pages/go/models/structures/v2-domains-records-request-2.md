# V2 Domains Records Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DomainsRecordsRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | `string` | Required | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `Flags` | `*int` | Required | An unsigned integer between 0-255 used for CAA records. |
| `Id` | `*int` | Optional, Read-only | A unique identifier for each domain record. |
| `Name` | `string` | Required | The host name, alias, or service being defined by the record. |
| `Port` | `models.Optional[int]` | Optional | The port for SRV records. |
| `Priority` | `models.Optional[int]` | Optional | The priority for SRV and MX records. |
| `Tag` | `*string` | Required | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
| `Ttl` | `*int` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `Type` | `string` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `Weight` | `models.Optional[int]` | Optional | The weight for SRV records. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DomainsRecordsRequest2 := models.V2DomainsRecordsRequest2{
        Data:                  "ns1.digitalocean.com",
        Flags:                 nil,
        Id:                    models.ToPointer(28448429),
        Name:                  "@",
        Port:                  models.NewOptional(models.ToPointer(74)),
        Priority:              models.NewOptional(models.ToPointer(100)),
        Tag:                   nil,
        Ttl:                   models.ToPointer(1800),
        Type:                  "NS",
        Weight:                models.NewOptional(models.ToPointer(218)),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



