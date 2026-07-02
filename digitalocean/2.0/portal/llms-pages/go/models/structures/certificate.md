# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the certificate was created. |
| `DnsNames` | `[]string` | Optional | An array of fully qualified domain names (FQDNs) for which the certificate was issued. |
| `Id` | `*uuid.UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a certificate. |
| `Name` | `*string` | Optional | A unique human-readable name referring to a certificate. |
| `NotAfter` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents the certificate's expiration date. |
| `Sha1Fingerprint` | `*string` | Optional, Read-only | A unique identifier generated from the SHA-1 fingerprint of the certificate. |
| `State` | [`*models.State`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/state.md) | Optional, Read-only | A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`. |
| `Type` | [`*models.Type4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. |
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
    certificate := models.Certificate{
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2017-02-08T16:02:37Z", func(err error) { log.Fatalln(err) })),
        DnsNames:              []string{
            "www.example.com",
            "example.com",
        },
        Id:                    models.ToPointer(uuid.MustParse("892071a0-bb95-49bc-8021-3afd67a210bf")),
        Name:                  models.ToPointer("web-cert-01"),
        NotAfter:              models.ToPointer(parseTime(time.RFC3339, "2017-02-22T00:23:00Z", func(err error) { log.Fatalln(err) })),
        Sha1Fingerprint:       models.ToPointer("dfcc9f57d86bf58e321c2c6c31c7a971be244ac7"),
        State:                 models.ToPointer(models.State_Verified),
        Type:                  models.ToPointer(models.Type4_LetsEncrypt),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



