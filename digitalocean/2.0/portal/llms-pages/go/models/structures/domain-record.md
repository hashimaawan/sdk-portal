# Domain Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRvbWFpblJlY29yZA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`DomainRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | `*string` | Optional | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `Flags` | `models.Optional[int]` | Optional | An unsigned integer between 0-255 used for CAA records. |
| `Id` | `*int` | Optional, Read-only | A unique identifier for each domain record. |
| `Name` | `*string` | Optional | The host name, alias, or service being defined by the record. |
| `Port` | `models.Optional[int]` | Optional | The port for SRV records. |
| `Priority` | `models.Optional[int]` | Optional | The priority for SRV and MX records. |
| `Tag` | `models.Optional[string]` | Optional | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
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
    domainRecord := models.DomainRecord{
        Data:                  models.ToPointer("ns1.digitalocean.com"),
        Flags:                 models.NewOptional(models.ToPointer(32)),
        Id:                    models.ToPointer(28448429),
        Name:                  models.ToPointer("@"),
        Port:                  models.NewOptional(models.ToPointer(164)),
        Ttl:                   models.ToPointer(1800),
        Type:                  "NS",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



