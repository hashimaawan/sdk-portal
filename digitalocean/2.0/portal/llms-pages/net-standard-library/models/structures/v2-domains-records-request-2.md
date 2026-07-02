# V2 Domains Records Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2DomainsRecordsRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | `string` | Required | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `Flags` | `int?` | Required | An unsigned integer between 0-255 used for CAA records. |
| `Id` | `int?` | Optional, Read-only | A unique identifier for each domain record. |
| `Name` | `string` | Required | The host name, alias, or service being defined by the record. |
| `Port` | `int?` | Optional | The port for SRV records. |
| `Priority` | `int?` | Optional | The priority for SRV and MX records. |
| `Tag` | `string` | Required | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
| `Ttl` | `int?` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `Type` | `string` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `Weight` | `int?` | Optional | The weight for SRV records. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2DomainsRecordsRequest2 v2DomainsRecordsRequest2 = new V2DomainsRecordsRequest2
{
    Data = "ns1.digitalocean.com",
    Flags = null,
    Name = "@",
    Tag = null,
    Type = "NS",
    Id = 28448429,
    Port = 74,
    Priority = 100,
    Ttl = 1800,
    Weight = 218,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



