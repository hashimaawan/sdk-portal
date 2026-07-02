# V2 Volumes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2VolumesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `string` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. |
| `Description` | `string` | Optional | An optional free-form text field to describe a block storage volume. |
| `DropletIds` | `List<int>` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. |
| `Id` | `string` | Optional, Read-only | The unique identifier for the block storage volume. |
| `Name` | `string` | Required | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. |
| `SizeGigabytes` | `int` | Required | The size of the block storage volume in GiB (1024^3). |
| `Tags` | `List<string>` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `SnapshotId` | `string` | Optional | The unique identifier for the volume snapshot from which to create the volume. |
| `FilesystemType` | `string` | Optional | The name of the filesystem type to be used on the volume. When provided, the volume will automatically be formatted to the specified filesystem type. Currently, the available options are `ext4` and `xfs`. Pre-formatted volumes are automatically mounted when attached to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS Droplets created on or after April 26, 2018. Attaching pre-formatted volumes to other Droplets is not recommended. |
| `FilesystemLabel` | `string` | Optional | **Constraints**: *Maximum Length*: `16` |
| `Region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2VolumesRequest v2VolumesRequest = new V2VolumesRequest
{
    Name = "example",
    SizeGigabytes = 10,
    Region = Region2.Nyc3,
    CreatedAt = "2020-03-02T17:00:49Z",
    Description = "Block store for examples",
    DropletIds = new List<int>
    {

    },
    Id = "506f78a4-e098-11e5-ad9f-000f53306ae1",
    Tags = new List<string>
    {
        "base-image",
        "prod",
    },
    SnapshotId = "b0798135-fb76-11eb-946a-0a58ac146f33",
    FilesystemType = "ext4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



