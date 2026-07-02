# Latest Manifest

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxhdGVzdE1hbmlmZXN0

*This model accepts additional fields of type Object.*


# Class Name

`LatestManifest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Blobs` | [`List<Blob>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/blob.md) | Optional | All blobs associated with this manifest | List<Blob> getBlobs() | setBlobs(List<Blob> blobs) |
| `CompressedSizeBytes` | `Integer` | Optional | The compressed size of the manifest in bytes. | Integer getCompressedSizeBytes() | setCompressedSizeBytes(Integer compressedSizeBytes) |
| `Digest` | `String` | Optional | The manifest digest | String getDigest() | setDigest(String digest) |
| `RegistryName` | `String` | Optional | The name of the container registry. | String getRegistryName() | setRegistryName(String registryName) |
| `Repository` | `String` | Optional | The name of the repository. | String getRepository() | setRepository(String repository) |
| `SizeBytes` | `Integer` | Optional | The uncompressed size of the manifest in bytes (this size is calculated asynchronously so it may not be immediately available). | Integer getSizeBytes() | setSizeBytes(Integer sizeBytes) |
| `Tags` | `List<String>` | Optional | All tags associated with this manifest | List<String> getTags() | setTags(List<String> tags) |
| `UpdatedAt` | `LocalDateTime` | Optional | The time the manifest was last updated. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Blob;
import com.digitalocean.api.models.LatestManifest;
import java.io.IOException;
import java.util.Arrays;

LatestManifest latestManifest = new LatestManifest.Builder()
    .blobs(Arrays.asList(
        new Blob.Builder()
            .compressedSizeBytes(12)
            .digest("digest2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Blob.Builder()
            .compressedSizeBytes(12)
            .digest("digest2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .compressedSizeBytes(2803255)
    .digest("sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221")
    .registryName("example")
    .repository("repo-1")
    .sizeBytes(5861888)
    .tags(Arrays.asList(
        "latest",
        "v1",
        "v2"
    ))
    .updatedAt(DateTimeHelper.fromRfc8601DateTime("2020-04-09T23:54:25Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



