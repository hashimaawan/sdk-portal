# Repository

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlcG9zaXRvcnk

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Repository`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LatestTag` | [`LatestTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/latest-tag.md) | Optional | - |
| `Name` | `string` | Optional | The name of the repository. |
| `RegistryName` | `string` | Optional | The name of the container registry. |
| `TagCount` | `int?` | Optional | The number of tags in the repository. |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Repository repository = new Repository
{
    LatestTag = new LatestTag
    {
        CompressedSizeBytes = 108,
        ManifestDigest = "manifest_digest2",
        RegistryName = "registry_name4",
        Repository = "repository4",
        SizeBytes = 226,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Name = "repo-1",
    RegistryName = "example",
    TagCount = 1,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



