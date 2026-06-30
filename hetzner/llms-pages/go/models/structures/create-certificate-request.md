# Create Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVxdWVzdA


# Class Name

`CreateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificate` | `*string` | Optional | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding. Required for type `uploaded` Certificates. |
| `DomainNames` | `[]string` | Optional | Domains and subdomains that should be contained in the Certificate issued by *Let's Encrypt*. Required for type `managed` Certificates. |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Certificate |
| `PrivateKey` | `*string` | Optional | Certificate key in PEM format. Required for type `uploaded` Certificates. |
| `Type` | [`*models.Type1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-1.md) | Optional | Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createCertificateRequest := models.CreateCertificateRequest{
        Certificate:          models.ToPointer("-----BEGIN CERTIFICATE-----\n..."),
        DomainNames:          []string{
            "domain_names8",
            "domain_names9",
            "domain_names0",
        },
        Labels:               models.ToPointer(interface{}("[key1, val1][key2, val2]")),
        Name:                 "my website cert",
        PrivateKey:           models.ToPointer("-----BEGIN PRIVATE KEY-----\n..."),
        Type:                 models.ToPointer(models.Type1Enum_UPLOADED),
    }

}
```



