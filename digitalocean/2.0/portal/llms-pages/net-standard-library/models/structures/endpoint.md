# Endpoint

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkVuZHBvaW50

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Endpoint`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CertificateId` | `Guid?` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. |
| `CreatedAt` | `DateTime?` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the CDN endpoint was created. |
| `CustomDomain` | `string` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. |
| `Endpoint` | `string` | Optional, Read-only | The fully qualified domain name (FQDN) from which the CDN-backed content is served. |
| `Id` | `Guid?` | Optional, Read-only | A unique ID that can be used to identify and reference a CDN endpoint. |
| `Origin` | `string` | Required | The fully qualified domain name (FQDN) for the origin server which provides the content for the CDN. This is currently restricted to a Space. |
| `Ttl` | [`Ttl?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl.Enum_3600` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

Endpoint endpoint = new Endpoint
{
    Origin = "static-images.nyc3.digitaloceanspaces.com",
    CertificateId = new Guid("892071a0-bb95-49bc-8021-3afd67a210bf"),
    CreatedAt = DateTime.ParseExact("2018-03-21T16:02:37Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    CustomDomain = "static.example.com",
    Endpoint = "static-images.nyc3.cdn.digitaloceanspaces.com",
    Id = new Guid("892071a0-bb95-49bc-8021-3afd67a210bf"),
    Ttl = Ttl.Enum3600,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



