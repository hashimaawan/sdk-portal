# V2 Volumes Actions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2VolumesActionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Region` | [`Region2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. |
| `Type` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-21.md) | Required | The volume action to initiate. |
| `DropletId` | `int` | Required | The unique identifier for the Droplet the volume will be attached or detached from. |
| `Tags` | `List<string>` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2VolumesActionsRequest v2VolumesActionsRequest = new V2VolumesActionsRequest
{
    Type = Type21.Attach,
    DropletId = 11612190,
    Region = Region2.Nyc3,
    Tags = new List<string>
    {
        "base-image",
        "prod",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



