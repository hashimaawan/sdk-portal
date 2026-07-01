# Certificates Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlc1Jlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`CertificatesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificates` | [`List<Certificate>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/certificate.md) | Required | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
using System.Collections.Generic;

CertificatesResponse certificatesResponse = new CertificatesResponse
{
    Certificates = new List<Certificate>
    {
        new Certificate
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
                ["key0"] = "labels2",
                ["key1"] = "labels1",
                ["key2"] = "labels0",
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
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            Status = new Status2
            {
                Error = null,
                Issuance = Issuance.Completed,
                Renewal = Renewal.Failed,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Type = HetznerCloudApi.Standard.Models.Type.Uploaded,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Meta = new Meta
    {
        Pagination = new Pagination
        {
            LastPage = 77.7,
            NextPage = 209.18,
            Page = 17.58,
            PerPage = 13.34,
            PreviousPage = 50.02,
            TotalEntries = 206.64,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



