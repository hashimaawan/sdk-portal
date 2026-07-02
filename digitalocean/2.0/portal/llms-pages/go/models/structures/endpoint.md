# Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkVuZHBvaW50

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Endpoint`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CertificateId` | `*uuid.UUID` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the CDN endpoint was created. |
| `CustomDomain` | `*string` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. |
| `Endpoint` | `*string` | Optional, Read-only | The fully qualified domain name (FQDN) from which the CDN-backed content is served. |
| `Id` | `*uuid.UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a CDN endpoint. |
| `Origin` | `string` | Required | The fully qualified domain name (FQDN) for the origin server which provides the content for the CDN. This is currently restricted to a Space. |
| `Ttl` | [`*models.Ttl`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `3600` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
    "github.com/google/uuid"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    endpoint := models.Endpoint{
        CertificateId:         models.ToPointer(uuid.MustParse("892071a0-bb95-49bc-8021-3afd67a210bf")),
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2018-03-21T16:02:37Z", func(err error) { log.Fatalln(err) })),
        CustomDomain:          models.ToPointer("static.example.com"),
        Endpoint:              models.ToPointer("static-images.nyc3.cdn.digitaloceanspaces.com"),
        Id:                    models.ToPointer(uuid.MustParse("892071a0-bb95-49bc-8021-3afd67a210bf")),
        Origin:                "static-images.nyc3.digitaloceanspaces.com",
        Ttl:                   models.ToPointer(models.Ttl_Enum3600),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



