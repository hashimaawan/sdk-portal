# Action 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFjdGlvbjI

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Action2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CompletedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was completed. |
| `Id` | `int?` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/region.md) | Optional | - |
| `RegionSlug` | `string` | Optional | - |
| `ResourceId` | `int?` | Optional | A unique identifier for the resource that the action is associated with. |
| `ResourceType` | `string` | Optional | The type of resource that the action is associated with. |
| `StartedAt` | `DateTime?` | Optional | A time value given in ISO8601 combined date and time format that represents when the action was initiated. |
| `Status` | [`Status1?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/status-1.md) | Optional | The current status of the action. This can be "in-progress", "completed", or "errored".<br><br>**Default**: `Status1.inprogress` |
| `Type` | `string` | Optional | This is the type of action that the object represents. For example, this could be "transfer" to represent the state of an image transfer action. |
| `ProjectId` | `Guid?` | Optional | The UUID of the project to which the reserved IP currently belongs. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

Action2 action2 = new Action2
{
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
    RegionSlug = "region_slug8",
    ResourceId = 3164444,
    ResourceType = "droplet",
    StartedAt = DateTime.ParseExact("2020-11-14T16:29:21Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Status = Status1.Completed,
    Type = "create",
    ProjectId = new Guid("746c6152-2fa2-11ed-92d3-27aaa54e4988"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



