# Snapshot

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNuYXBzaG90

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Snapshot`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Required | The unique identifier for the snapshot. |
| `CreatedAt` | `DateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the snapshot was created. |
| `MinDiskSize` | `int` | Required | The minimum size in GB required for a volume or Droplet to use this snapshot. |
| `Name` | `string` | Required | A human-readable name for the snapshot. |
| `Regions` | `List<string>` | Required | An array of the regions that the snapshot is available in. The regions are represented by their identifying slug values. |
| `SizeGigabytes` | `double` | Required | The billable size of the snapshot in gigabytes. |
| `ResourceId` | `string` | Required | The unique identifier for the resource that the snapshot originated from. |
| `ResourceType` | [`ResourceType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/resource-type-1.md) | Required | The type of resource that the snapshot originated from. |
| `Tags` | `List<string>` | Required | An array of Tags the snapshot has been tagged with. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Snapshot snapshot = new Snapshot
{
    Id = "6372321",
    CreatedAt = DateTime.ParseExact("2020-07-28T16:47:44Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    MinDiskSize = 25,
    Name = "web-01-1595954862243",
    Regions = new List<string>
    {
        "nyc3",
        "sfo3",
    },
    SizeGigabytes = 2.34,
    ResourceId = "200776916",
    ResourceType = ResourceType1.Droplet,
    Tags = new List<string>
    {
        "web",
        "env:prod",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



