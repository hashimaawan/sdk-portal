# Create Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVzcG9uc2U


# Class Name

`CreateCertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/nullable-action.md) | Optional | - |
| `Certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/certificate.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

CreateCertificateResponse createCertificateResponse = new CreateCertificateResponse
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
    Action = new NullableAction
    {
        Command = "command6",
        Error = new Error
        {
            Code = "code2",
            Message = "message4",
        },
        Finished = "finished0",
        Id = 238,
        Progress = 143.26,
        Resources = new List<Resource>
        {
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
            new Resource
            {
                Id = 198,
                Type = "type0",
            },
        },
        Started = "started8",
        Status = StatusEnum.Running,
    },
};
```



