# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `string` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. |
| `Description` | `string` | Optional | An optional free-form text field to describe a block storage volume. |
| `DropletIds` | `List<int>` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. |
| `Id` | `string` | Optional, Read-only | The unique identifier for the block storage volume. |
| `Name` | `string` | Optional | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. |
| `SizeGigabytes` | `int?` | Optional | The size of the block storage volume in GiB (1024^3). |
| `Tags` | `List<string>` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `FilesystemLabel` | `string` | Optional | The label currently applied to the filesystem. |
| `FilesystemType` | `string` | Optional | The type of filesystem currently in-use on the volume. |
| `Region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/region.md) | Optional, Read-only | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Volume volume = new Volume
{
    CreatedAt = "2020-03-02T17:00:49Z",
    Description = "Block store for examples",
    DropletIds = new List<int>
    {

    },
    Id = "506f78a4-e098-11e5-ad9f-000f53306ae1",
    Name = "example",
    SizeGigabytes = 10,
    Tags = new List<string>
    {
        "base-image",
        "prod",
    },
    FilesystemLabel = "example",
    FilesystemType = "ext4",
    Region = new Region
    {
        Available = true,
        Features = new List<string>
        {
            "private_networking",
            "backups",
            "ipv6",
            "metadata",
        },
        Name = "New York 1",
        Sizes = new List<string>
        {
            "s-1vcpu-1gb",
            "s-1vcpu-2gb",
            "s-1vcpu-3gb",
            "s-2vcpu-2gb",
            "s-3vcpu-1gb",
            "s-2vcpu-4gb",
            "s-4vcpu-8gb",
            "s-6vcpu-16gb",
            "s-8vcpu-32gb",
            "s-12vcpu-48gb",
            "s-16vcpu-64gb",
            "s-20vcpu-96gb",
            "s-24vcpu-128gb",
            "s-32vcpu-192gb",
        },
        Slug = "nyc1",
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



