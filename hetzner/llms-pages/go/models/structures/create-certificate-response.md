# Create Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVzcG9uc2U


# Class Name

`CreateCertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`models.Optional[models.NullableAction]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/nullable-action.md) | Optional | - |
| `Certificate` | [`models.Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/certificate.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createCertificateResponse := models.CreateCertificateResponse{
        Action:               models.NewOptional(models.ToPointer(models.NullableAction{
            Command:              "command6",
            Error:                models.ToPointer(models.Error{
                Code:                 "code2",
                Message:              "message4",
            }),
            Finished:             models.ToPointer("finished0"),
            Id:                   238,
            Progress:             float64(143.26),
            Resources:            []models.Resource{
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
            },
            Started:              "started8",
            Status:               models.StatusEnum_RUNNING,
        })),
        Certificate:          models.Certificate{
            Certificate:          models.ToPointer("-----BEGIN CERTIFICATE-----\n..."),
            Created:              "2016-01-30T23:55:00+00:00",
            DomainNames:          []string{
                "example.com",
                "webmail.example.com",
                "www.example.com",
            },
            Fingerprint:          models.ToPointer("03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f"),
            Id:                   42,
            Labels:               map[string]string{
                "key0": "labels8",
                "key1": "labels7",
                "key2": "labels6",
            },
            Name:                 "my-resource",
            NotValidAfter:        models.ToPointer("2019-07-08T09:59:59+00:00"),
            NotValidBefore:       models.ToPointer("2019-01-08T10:00:00+00:00"),
            Status:               models.NewOptional(models.ToPointer(models.Status2{
                Error:                models.NewOptional[models.Error2](nil),
                Issuance:             models.ToPointer(models.IssuanceEnum_COMPLETED),
                Renewal:              models.ToPointer(models.RenewalEnum_FAILED),
            })),
            Type:                 models.ToPointer(models.TypeEnum_UPLOADED),
            UsedBy:               []models.UsedBy{
                models.UsedBy{
                    Id:                   4711,
                    Type:                 "load_balancer",
                },
            },
        },
    }

}
```



