# V2 Cdn Endpoints Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBDZG4lMjUyMEVuZHBvaW50cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2CdnEndpointsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CertificateId` | `Guid?` | Optional | The ID of a DigitalOcean managed TLS certificate used for SSL when a custom subdomain is provided. |
| `CustomDomain` | `string` | Optional | The fully qualified domain name (FQDN) of the custom subdomain used with the CDN endpoint. |
| `Ttl` | [`Ttl?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/ttl.md) | Optional | The amount of time the content is cached by the CDN's edge servers in seconds. TTL must be one of 60, 600, 3600, 86400, or 604800. Defaults to 3600 (one hour) when excluded.<br><br>**Default**: `Ttl.Enum_3600` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2CdnEndpointsRequest v2CdnEndpointsRequest = new V2CdnEndpointsRequest
{
    CertificateId = new Guid("892071a0-bb95-49bc-8021-3afd67a210bf"),
    CustomDomain = "static.example.com",
    Ttl = Ttl.Enum3600,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



