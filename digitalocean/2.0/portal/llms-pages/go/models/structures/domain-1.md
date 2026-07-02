# Domain 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRvbWFpbjE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Domain1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpAddress` | `*string` | Optional | This optional attribute may contain an IP address. When provided, an A record will be automatically created pointing to the apex domain. |
| `Name` | `*string` | Optional | The name of the domain itself. This should follow the standard domain format of domain.TLD. For instance, `example.com` is a valid domain name. |
| `Ttl` | `models.Optional[int]` | Optional, Read-only | This value is the time to live for the records on this domain, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `ZoneFile` | `models.Optional[string]` | Optional, Read-only | This attribute contains the complete contents of the zone file for the selected domain. Individual domain record resources should be used to get more granular control over records. However, this attribute can also be used to get information about the SOA record, which is created automatically and is not accessible as an individual record resource. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    domain1 := models.Domain1{
        IpAddress:             models.ToPointer("192.0.2.1"),
        Name:                  models.ToPointer("example.com"),
        Ttl:                   models.NewOptional(models.ToPointer(1800)),
        ZoneFile:              models.NewOptional(models.ToPointer("$ORIGIN example.com.\n$TTL 1800\nexample.com. IN SOA ns1.digitalocean.com. hostmaster.example.com. 1415982609 10800 3600 604800 1800\nexample.com. 1800 IN NS ns1.digitalocean.com.\nexample.com. 1800 IN NS ns2.digitalocean.com.\nexample.com. 1800 IN NS ns3.digitalocean.com.\nexample.com. 1800 IN A 1.2.3.4\n")),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



