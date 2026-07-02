# Latest Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkxhdGVzdFRhZw

*This model accepts additional fields of type Object.*


# Class Name

`LatestTag`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CompressedSizeBytes` | `Integer` | Optional | The compressed size of the tag in bytes. | Integer getCompressedSizeBytes() | setCompressedSizeBytes(Integer compressedSizeBytes) |
| `ManifestDigest` | `String` | Optional | The digest of the manifest associated with the tag. | String getManifestDigest() | setManifestDigest(String manifestDigest) |
| `RegistryName` | `String` | Optional | The name of the container registry. | String getRegistryName() | setRegistryName(String registryName) |
| `Repository` | `String` | Optional | The name of the repository. | String getRepository() | setRepository(String repository) |
| `SizeBytes` | `Integer` | Optional | The uncompressed size of the tag in bytes (this size is calculated asynchronously so it may not be immediately available). | Integer getSizeBytes() | setSizeBytes(Integer sizeBytes) |
| `Tag` | `String` | Optional | The name of the tag. | String getTag() | setTag(String tag) |
| `UpdatedAt` | `LocalDateTime` | Optional | The time the tag was last updated. | LocalDateTime getUpdatedAt() | setUpdatedAt(LocalDateTime updatedAt) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.LatestTag;
import java.io.IOException;

LatestTag latestTag = new LatestTag.Builder()
    .compressedSizeBytes(2803255)
    .manifestDigest("sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221")
    .registryName("example")
    .repository("repo-1")
    .sizeBytes(5861888)
    .tag("latest")
    .updatedAt(DateTimeHelper.fromRfc8601DateTime("2020-04-09T23:54:25Z"))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



