# Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlUmVzcG9uc2U

*This model accepts additional fields of type object.*


# Class Name

`CertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/certificate.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
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
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



