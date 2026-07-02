# V2 Registry Digests Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRGlnZXN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2RegistryDigestsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Manifests` | [`List<LatestManifest>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/latest-manifest.md) | Optional | - |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/links.md) | Optional | - |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Models.Containers;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

V2RegistryDigestsResponse v2RegistryDigestsResponse = new V2RegistryDigestsResponse
{
    Meta = new Meta
    {
        Total = 3,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Manifests = new List<LatestManifest>
    {
        new LatestManifest
        {
            Blobs = new List<Blob>
            {
                new Blob
                {
                    CompressedSizeBytes = 1471,
                    Digest = "sha256:14119a10abf4669e8cdbdff324a9f9605d99697215a0d21c360fe8dfa8471bab",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new Blob
                {
                    CompressedSizeBytes = 12,
                    Digest = "sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e",
                    ["compressed_size_byte"] = ApiHelper.JsonDeserialize<object>("2814446"),
                },
                new Blob
                {
                    CompressedSizeBytes = 528,
                    Digest = "sha256:69704ef328d05a9f806b6b8502915e6a0a4faa4d72018dc42343f511490daf8a",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            CompressedSizeBytes = 1972332,
            Digest = "sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221",
            RegistryName = "example",
            Repository = "repo-1",
            SizeBytes = 2816445,
            Tags = new List<string>
            {
                "v1",
                "v2",
            },
            UpdatedAt = DateTime.ParseExact("2021-04-09T23:54:25Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    Links = new Links
    {
        Pages = LinksPages.FromPages(
            new Pages
            {
                Last = "https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1",
                Next = "https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1",
                ["first"] = ApiHelper.JsonDeserialize<object>("\"https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1\""),
                ["prev"] = ApiHelper.JsonDeserialize<object>("\"https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1\""),
            }
        ),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



