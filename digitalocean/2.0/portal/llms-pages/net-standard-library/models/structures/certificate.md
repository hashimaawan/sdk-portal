# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the certificate was created. |
| `DnsNames` | `List<string>` | Optional | An array of fully qualified domain names (FQDNs) for which the certificate was issued. |
| `Id` | `Guid?` | Optional, Read-only | A unique ID that can be used to identify and reference a certificate. |
| `Name` | `string` | Optional | A unique human-readable name referring to a certificate. |
| `NotAfter` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents the certificate's expiration date. |
| `Sha1Fingerprint` | `string` | Optional, Read-only | A unique identifier generated from the SHA-1 fingerprint of the certificate. |
| `State` | [`State?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/state.md) | Optional, Read-only | A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`. |
| `Type` | [`Type4?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Certificate certificate = new Certificate
{
    CreatedAt = DateTime.ParseExact("2017-02-08T16:02:37Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    DnsNames = new List<string>
    {
        "www.example.com",
        "example.com",
    },
    Id = new Guid("892071a0-bb95-49bc-8021-3afd67a210bf"),
    Name = "web-cert-01",
    NotAfter = DateTime.ParseExact("2017-02-22T00:23:00Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Sha1Fingerprint = "dfcc9f57d86bf58e321c2c6c31c7a971be244ac7",
    State = State.Verified,
    Type = Type4.LetsEncrypt,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



