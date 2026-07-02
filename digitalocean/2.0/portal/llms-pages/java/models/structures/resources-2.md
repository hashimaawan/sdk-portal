# Resources 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc291cmNlczI

An embedded object containing key value pairs of resource type and resource statistics. It also includes a count of the total number of resources tagged with the current tag as well as a `last_tagged_uri` attribute set to the last resource tagged with the current tag.

*This model accepts additional fields of type Object.*


# Class Name

`Resources2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Count` | `Integer` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` | Integer getCount() | setCount(Integer count) |
| `LastTaggedUri` | `String` | Optional | The URI for the last tagged object for this type of resource. | String getLastTaggedUri() | setLastTaggedUri(String lastTaggedUri) |
| `Databases` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | Databases getDatabases() | setDatabases(Databases databases) |
| `Droplets` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | Databases getDroplets() | setDroplets(Databases droplets) |
| `Imgages` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | Databases getImgages() | setImgages(Databases imgages) |
| `VolumeSnapshots` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | Databases getVolumeSnapshots() | setVolumeSnapshots(Databases volumeSnapshots) |
| `Volumes` | [`Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. | Databases getVolumes() | setVolumes(Databases volumes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Databases;
import com.digitalocean.api.models.Resources2;
import java.io.IOException;

Resources2 resources2 = new Resources2.Builder()
    .count(5)
    .lastTaggedUri("https://api.digitalocean.com/v2/images/7555620")
    .databases(new Databases.Builder()
        .count(1)
        .lastTaggedUri("https://api.digitalocean.com/v2/databases/b92438f6-ba03-416c-b642-e9236db91976")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .droplets(new Databases.Builder()
        .count(1)
        .lastTaggedUri("https://api.digitalocean.com/v2/droplets/3164444")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .imgages(new Databases.Builder()
        .count(158)
        .lastTaggedUri("last_tagged_uri4")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .volumeSnapshots(new Databases.Builder()
        .count(1)
        .lastTaggedUri("https://api.digitalocean.com/v2/snapshots/1f6f46e8-6b60-11e9-be4e-0a58ac144519")
        .build())
    .volumes(new Databases.Builder()
        .count(1)
        .lastTaggedUri("https://api.digitalocean.com/v2/volumes/3d80cb72-342b-4aaa-b92e-4e4abb24a933")
        .build())
.additionalProperty("images", ApiHelper.deserialize("{\"count\":1,\"last_tagged_uri\":\"https://api.digitalocean.com/v2/images/7555620\"}"))
    .build();
```



