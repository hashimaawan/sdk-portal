# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Certificate` | `string` | Required | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `DomainNames` | `List<string>` | Required | Domains and subdomains covered by the Certificate |
| `Fingerprint` | `string` | Required | SHA256 fingerprint of the Certificate |
| `Id` | `int` | Required | ID of the Resource |
| `Labels` | `Dictionary<string, string>` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `NotValidAfter` | `string` | Required | Point in time when the Certificate stops being valid (in ISO-8601 format) |
| `NotValidBefore` | `string` | Required | Point in time when the Certificate becomes valid (in ISO-8601 format) |
| `Status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/status-2.md) | Optional | Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates |
| `Type` | [`TypeEnum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type.md) | Optional | Type of the Certificate |
| `UsedBy` | [`List<UsedBy>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/used-by.md) | Required | Resources currently using the Certificate |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

Certificate certificate = new Certificate
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
};
```



