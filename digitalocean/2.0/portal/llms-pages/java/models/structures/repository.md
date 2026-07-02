# Repository

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlcG9zaXRvcnk

*This model accepts additional fields of type Object.*


# Class Name

`Repository`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `LatestTag` | [`LatestTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/latest-tag.md) | Optional | - | LatestTag getLatestTag() | setLatestTag(LatestTag latestTag) |
| `Name` | `String` | Optional | The name of the repository. | String getName() | setName(String name) |
| `RegistryName` | `String` | Optional | The name of the container registry. | String getRegistryName() | setRegistryName(String registryName) |
| `TagCount` | `Integer` | Optional | The number of tags in the repository. | Integer getTagCount() | setTagCount(Integer tagCount) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.LatestTag;
import com.digitalocean.api.models.Repository;
import java.io.IOException;

Repository repository = new Repository.Builder()
    .latestTag(new LatestTag.Builder()
        .compressedSizeBytes(108)
        .manifestDigest("manifest_digest2")
        .registryName("registry_name4")
        .repository("repository4")
        .sizeBytes(226)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .name("repo-1")
    .registryName("example")
    .tagCount(1)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



