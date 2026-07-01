# Create Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVxdWVzdA


# Class Name

`CreateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificate` | `string` | Optional | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding. Required for type `uploaded` Certificates. |
| `DomainNames` | `List<string>` | Optional | Domains and subdomains that should be contained in the Certificate issued by *Let's Encrypt*. Required for type `managed` Certificates. |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Certificate |
| `PrivateKey` | `string` | Optional | Certificate key in PEM format. Required for type `uploaded` Certificates. |
| `Type` | [`Type1Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-1.md) | Optional | Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Utilities;
using System.Collections.Generic;

CreateCertificateRequest createCertificateRequest = new CreateCertificateRequest
{
    Name = "my website cert",
    Certificate = "-----BEGIN CERTIFICATE-----\n...",
    DomainNames = new List<string>
    {
        "domain_names8",
        "domain_names9",
        "domain_names0",
    },
    Labels = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    PrivateKey = "-----BEGIN PRIVATE KEY-----\n...",
    Type = Type1Enum.Uploaded,
};
```



