# Repository 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlcG9zaXRvcnkx

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Repository1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LatestManifest` | [`LatestManifest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/latest-manifest.md) | Optional | - |
| `ManifestCount` | `int?` | Optional | The number of manifests in the repository. |
| `Name` | `string` | Optional | The name of the repository. |
| `RegistryName` | `string` | Optional | The name of the container registry. |
| `TagCount` | `int?` | Optional | The number of tags in the repository. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Repository1 repository1 = new Repository1
{
    LatestManifest = new LatestManifest
    {
        Blobs = new List<Blob>
        {
            new Blob
            {
                CompressedSizeBytes = 12,
                Digest = "digest2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Blob
            {
                CompressedSizeBytes = 12,
                Digest = "digest2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            new Blob
            {
                CompressedSizeBytes = 12,
                Digest = "digest2",
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        CompressedSizeBytes = 154,
        Digest = "digest0",
        RegistryName = "registry_name4",
        Repository = "repository4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ManifestCount = 1,
    Name = "repo-1",
    RegistryName = "example",
    TagCount = 1,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



