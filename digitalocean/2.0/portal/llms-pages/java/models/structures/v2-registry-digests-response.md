# V2 Registry Digests Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRGlnZXN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2RegistryDigestsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Manifests` | [`List<LatestManifest>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/latest-manifest.md) | Optional | - | List<LatestManifest> getManifests() | setManifests(List<LatestManifest> manifests) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Blob;
import com.digitalocean.api.models.LatestManifest;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.V2RegistryDigestsResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2RegistryDigestsResponse v2RegistryDigestsResponse = new V2RegistryDigestsResponse.Builder(
    new Meta.Builder(
        3
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.manifests(Arrays.asList(
        new LatestManifest.Builder()
            .blobs(Arrays.asList(
                new Blob.Builder()
                    .compressedSizeBytes(1471)
                    .digest("sha256:14119a10abf4669e8cdbdff324a9f9605d99697215a0d21c360fe8dfa8471bab")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build(),
                new Blob.Builder()
                    .compressedSizeBytes(12)
                    .digest("sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e")
                .additionalProperty("compressed_size_byte", ApiHelper.deserialize("2814446"))
                    .build(),
                new Blob.Builder()
                    .compressedSizeBytes(528)
                    .digest("sha256:69704ef328d05a9f806b6b8502915e6a0a4faa4d72018dc42343f511490daf8a")
                .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                    .build()
            ))
            .compressedSizeBytes(1972332)
            .digest("sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221")
            .registryName("example")
            .repository("repo-1")
            .sizeBytes(2816445)
            .tags(Arrays.asList(
                "v1",
                "v2"
            ))
            .updatedAt(DateTimeHelper.fromRfc8601DateTime("2021-04-09T23:54:25Z"))
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1")
                .next("https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1")
            .additionalProperty("first", ApiHelper.deserialize("\"https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1\""))
            .additionalProperty("prev", ApiHelper.deserialize("\"https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1\""))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



