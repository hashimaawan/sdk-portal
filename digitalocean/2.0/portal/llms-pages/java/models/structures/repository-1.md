# Repository 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlcG9zaXRvcnkx

*This model accepts additional fields of type Object.*


# Class Name

`Repository1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LatestManifest` | [`LatestManifest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/latest-manifest.md) | Optional | - | LatestManifest getLatestManifest() | setLatestManifest(LatestManifest latestManifest) |
| `ManifestCount` | `Integer` | Optional | The number of manifests in the repository. | Integer getManifestCount() | setManifestCount(Integer manifestCount) |
| `Name` | `String` | Optional | The name of the repository. | String getName() | setName(String name) |
| `RegistryName` | `String` | Optional | The name of the container registry. | String getRegistryName() | setRegistryName(String registryName) |
| `TagCount` | `Integer` | Optional | The number of tags in the repository. | Integer getTagCount() | setTagCount(Integer tagCount) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Blob;
import com.digitalocean.api.models.LatestManifest;
import com.digitalocean.api.models.Repository1;
import java.io.IOException;
import java.util.Arrays;

Repository1 repository1 = new Repository1.Builder()
    .latestManifest(new LatestManifest.Builder()
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
                .build(),
            new Blob.Builder()
                .compressedSizeBytes(12)
                .digest("digest2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
        .compressedSizeBytes(154)
        .digest("digest0")
        .registryName("registry_name4")
        .repository("repository4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .manifestCount(1)
    .name("repo-1")
    .registryName("example")
    .tagCount(1)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



