# Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlRhZw

A tag is a label that can be applied to a resource (currently Droplets, Images, Volumes, Volume Snapshots, and Database clusters) in order to better organize or facilitate the lookups and actions on it.
Tags have two attributes: a user defined `name` attribute and an embedded `resources` attribute with information about resources that have been tagged.

*This model accepts additional fields of type Object.*


# Class Name

`Tag`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Name` | `String` | Optional | The name of the tag. Tags may contain letters, numbers, colons, dashes, and underscores.<br>There is a limit of 255 characters per tag.<br><br>**Note:** Tag names are case stable, which means the capitalization you use when you first create a tag is canonical.<br><br>When working with tags in the API, you must use the tag's canonical capitalization. For example, if you create a tag named "PROD", the URL to add that tag to a resource would be `https://api.digitalocean.com/v2/tags/PROD/resources` (not `/v2/tags/prod/resources`).<br><br>Tagged resources in the control panel will always display the canonical capitalization. For example, if you create a tag named "PROD", you can tag resources in the control panel by entering "prod". The tag will still display with its canonical capitalization, "PROD".<br><br>**Constraints**: *Maximum Length*: `255`, *Pattern*: `^[a-zA-Z0-9_\-\:]+$` | String getName() | setName(String name) |
| `Resources` | [`Resources2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/resources-2.md) | Optional, Read-only | An embedded object containing key value pairs of resource type and resource statistics. It also includes a count of the total number of resources tagged with the current tag as well as a `last_tagged_uri` attribute set to the last resource tagged with the current tag. | Resources2 getResources() | setResources(Resources2 resources) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Databases;
import com.digitalocean.api.models.Resources2;
import com.digitalocean.api.models.Tag;
import java.io.IOException;

Tag tag = new Tag.Builder()
    .name("extra-awesome")
    .resources(new Resources2.Builder()
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
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



