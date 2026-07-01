# Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlUmVzcG9uc2U


# Class Name

`CertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/certificate.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

CertificateResponse certificateResponse = new CertificateResponse
{
    Certificate = new Certificate
    {
        CertificateProp = "-----BEGIN CERTIFICATE-----\n...",
        Created = "2016-01-30T23:55:00+00:00",
        DomainNames = new List<string>
        {
            "example.com",
            "webmail.example.com",
            "www.example.com",
        },
        Fingerprint = "03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f",
        Id = 42,
        Labels = new Dictionary<string, string>
        {
            ["key0"] = "labels8",
            ["key1"] = "labels7",
            ["key2"] = "labels6",
        },
        Name = "my-resource",
        NotValidAfter = "2019-07-08T09:59:59+00:00",
        NotValidBefore = "2019-01-08T10:00:00+00:00",
        UsedBy = new List<UsedBy>
        {
            new UsedBy
            {
                Id = 4711,
                Type = "load_balancer",
            },
        },
        Status = new Status2
        {
            Error = null,
            Issuance = IssuanceEnum.Completed,
            Renewal = RenewalEnum.Failed,
        },
        Type = TypeEnum.Uploaded,
    },
};
```



