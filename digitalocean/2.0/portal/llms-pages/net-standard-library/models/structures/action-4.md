# Action 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFjdGlvbjQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Action4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ResourceId` | `int?` | Optional | A unique identifier for the resource that the action is associated with. |
| `Type` | `string` | Optional | This is the type of action that the object represents. For example, this could be "attach_volume" to represent the state of a volume attach action. |
| `CompletedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. |
| `Id` | `int?` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/region.md) | Optional | - |
| `RegionSlug` | `string` | Optional | - |
| `ResourceType` | `string` | Optional | The type of resource that the action is associated with. |
| `StartedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. |
| `Status` | [`Status1?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `Status1.inprogress` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Action4 action4 = new Action4
{
    ResourceId = 160,
    Type = "attach_volume",
    CompletedAt = DateTime.ParseExact("2020-11-14T16:30:06Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Id = 36804636,
    Region = new Region
    {
        Available = false,
        Features = new List<string>
        {
            "features7",
            "features8",
            "features9",
        },
        Name = "name6",
        Sizes = new List<string>
        {
            "sizes6",
        },
        Slug = "slug0",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ResourceType = "droplet",
    StartedAt = DateTime.ParseExact("2020-11-14T16:29:21Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Status = Status1.Completed,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



