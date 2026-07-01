# Certificates Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlc1Jlc3BvbnNl


# Class Name

`CertificatesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificates` | [`[]models.Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/certificate.md) | Required | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    certificatesResponse := models.CertificatesResponse{
        Certificates:         []models.Certificate{
            models.Certificate{
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
                    "key0": "labels2",
                    "key1": "labels1",
                    "key2": "labels0",
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
        },
        Meta:                 models.ToPointer(models.Meta{
            Pagination:           models.Pagination{
                LastPage:             models.ToPointer(float64(77.7)),
                NextPage:             models.ToPointer(float64(209.18)),
                Page:                 float64(17.58),
                PerPage:              float64(13.34),
                PreviousPage:         models.ToPointer(float64(50.02)),
                TotalEntries:         models.ToPointer(float64(206.64)),
            },
        }),
    }

}
```



