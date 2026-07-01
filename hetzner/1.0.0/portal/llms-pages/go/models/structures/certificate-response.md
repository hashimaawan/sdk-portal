# Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`CertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificate` | [`models.Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/certificate.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    certificateResponse := models.CertificateResponse{
        Certificate:           models.Certificate{
            Certificate:           models.ToPointer("-----BEGIN CERTIFICATE-----\n..."),
            Created:               "2016-01-30T23:55:00+00:00",
            DomainNames:           []string{
                "example.com",
                "webmail.example.com",
                "www.example.com",
            },
            Fingerprint:           models.ToPointer("03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f"),
            Id:                    42,
            Labels:                map[string]string{
                "key0": "labels8",
                "key1": "labels7",
                "key2": "labels6",
            },
            Name:                  "my-resource",
            NotValidAfter:         models.ToPointer("2019-07-08T09:59:59+00:00"),
            NotValidBefore:        models.ToPointer("2019-01-08T10:00:00+00:00"),
            Status:                models.NewOptional(models.ToPointer(models.Status2{
                Error:                 models.NewOptional[models.Error2](nil),
                Issuance:              models.ToPointer(models.Issuance_Completed),
                Renewal:               models.ToPointer(models.Renewal_Failed),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            Type:                  models.ToPointer(models.Type_Uploaded),
            UsedBy:                []models.UsedBy{
                models.UsedBy{
                    Id:                    4711,
                    Type:                  "load_balancer",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



