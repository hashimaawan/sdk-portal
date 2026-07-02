# V2 Volumes Actions Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2VolumesActionsRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Region` | [`Region2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. |
| `Type` | [`Type21`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/type-21.md) | Required | The volume action to initiate. |
| `SizeGigabytes` | `int` | Required | The new size of the block storage volume in GiB (1024^3).<br><br>**Constraints**: `<= 16384` |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

V2VolumesActionsRequest2 v2VolumesActionsRequest2 = new V2VolumesActionsRequest2
{
    Type = Type21.Attach,
    SizeGigabytes = 15384,
    Region = Region2.Nyc3,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



