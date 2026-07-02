# Domain Record

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRvbWFpblJlY29yZA

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`DomainRecord`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | `string` | Optional | Variable data depending on record type. For example, the "data" value for an A record would be the IPv4 address to which the domain will be mapped. For a CAA record, it would contain the domain name of the CA being granted permission to issue certificates. |
| `Flags` | `int?` | Optional | An unsigned integer between 0-255 used for CAA records. |
| `Id` | `int?` | Optional, Read-only | A unique identifier for each domain record. |
| `Name` | `string` | Optional | The host name, alias, or service being defined by the record. |
| `Port` | `int?` | Optional | The port for SRV records. |
| `Priority` | `int?` | Optional | The priority for SRV and MX records. |
| `Tag` | `string` | Optional | The parameter tag for CAA records. Valid values are "issue", "issuewild", or "iodef" |
| `Ttl` | `int?` | Optional | This value is the time to live for the record, in seconds. This defines the time frame that clients can cache queried information before a refresh should be requested. |
| `Type` | `string` | Required | The type of the DNS record. For example: A, CNAME, TXT, ... |
| `Weight` | `int?` | Optional | The weight for SRV records. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

DomainRecord domainRecord = new DomainRecord
{
    Type = "NS",
    Data = "ns1.digitalocean.com",
    Flags = 32,
    Id = 28448429,
    Name = "@",
    Port = 164,
    Ttl = 1800,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



