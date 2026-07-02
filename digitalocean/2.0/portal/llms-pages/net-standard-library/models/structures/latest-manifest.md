# Latest Manifest

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxhdGVzdE1hbmlmZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`LatestManifest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Blobs` | [`List<Blob>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/blob.md) | Optional | All blobs associated with this manifest |
| `CompressedSizeBytes` | `int?` | Optional | The compressed size of the manifest in bytes. |
| `Digest` | `string` | Optional | The manifest digest |
| `RegistryName` | `string` | Optional | The name of the container registry. |
| `Repository` | `string` | Optional | The name of the repository. |
| `SizeBytes` | `int?` | Optional | The uncompressed size of the manifest in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `Tags` | `List<string>` | Optional | All tags associated with this manifest |
| `UpdatedAt` | `DateTime?` | Optional | The time the manifest was last updated. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

LatestManifest latestManifest = new LatestManifest
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
    },
    CompressedSizeBytes = 2803255,
    Digest = "sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221",
    RegistryName = "example",
    Repository = "repo-1",
    SizeBytes = 5861888,
    Tags = new List<string>
    {
        "latest",
        "v1",
        "v2",
    },
    UpdatedAt = DateTime.ParseExact("2020-04-09T23:54:25Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



