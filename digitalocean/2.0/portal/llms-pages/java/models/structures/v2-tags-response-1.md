# V2 Tags Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2TagsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Tag` | [`Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/tag.md) | Optional | A tag is a label that can be applied to a resource (currently Droplets, Images, Volumes, Volume Snapshots, and Database clusters) in order to better organize or facilitate the lookups and actions on it.<br>Tags have two attributes: a user defined `name` attribute and an embedded `resources` attribute with information about resources that have been tagged. | Tag getTag() | setTag(Tag tag) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Databases;
import com.digitalocean.api.models.Resources2;
import com.digitalocean.api.models.Tag;
import com.digitalocean.api.models.V2TagsResponse1;
import java.io.IOException;

V2TagsResponse1 v2TagsResponse1 = new V2TagsResponse1.Builder()
    .tag(new Tag.Builder()
        .name("extra-awesome")
        .resources(new Resources2.Builder()
            .count(0)
            .lastTaggedUri("last_tagged_uri6")
            .databases(new Databases.Builder()
                .count(0)
                .lastTaggedUri("last_tagged_uri2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .droplets(new Databases.Builder()
                .count(0)
                .lastTaggedUri("last_tagged_uri6")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .imgages(new Databases.Builder()
                .count(158)
                .lastTaggedUri("last_tagged_uri4")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build())
            .volumeSnapshots(new Databases.Builder()
                .count(0)
                .build())
            .volumes(new Databases.Builder()
                .count(0)
                .build())
        .additionalProperty("images", ApiHelper.deserialize("{\"count\":0}"))
            .build())
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



