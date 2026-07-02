# Latest Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxhdGVzdFRhZw

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`LatestTag`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CompressedSizeBytes` | `int?` | Optional | The compressed size of the tag in bytes. |
| `ManifestDigest` | `string` | Optional | The digest of the manifest associated with the tag. |
| `RegistryName` | `string` | Optional | The name of the container registry. |
| `Repository` | `string` | Optional | The name of the repository. |
| `SizeBytes` | `int?` | Optional | The uncompressed size of the tag in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `Tag` | `string` | Optional | The name of the tag. |
| `UpdatedAt` | `DateTime?` | Optional | The time the tag was last updated. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Globalization;

LatestTag latestTag = new LatestTag
{
    CompressedSizeBytes = 2803255,
    ManifestDigest = "sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221",
    RegistryName = "example",
    Repository = "repo-1",
    SizeBytes = 5861888,
    Tag = "latest",
    UpdatedAt = DateTime.ParseExact("2020-04-09T23:54:25Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



