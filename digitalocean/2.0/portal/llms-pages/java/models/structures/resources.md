# Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlc291cmNlcw

An object containing additional information about resource related to a Droplet requested to be destroyed.

*This model accepts additional fields of type Object.*


# Class Name

`Resources`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `FloatingIps` | [`List<Droplet1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet-1.md) | Optional | - | List<Droplet1> getFloatingIps() | setFloatingIps(List<Droplet1> floatingIps) |
| `ReservedIps` | [`List<Droplet1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet-1.md) | Optional | - | List<Droplet1> getReservedIps() | setReservedIps(List<Droplet1> reservedIps) |
| `Snapshots` | [`List<Droplet1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet-1.md) | Optional | - | List<Droplet1> getSnapshots() | setSnapshots(List<Droplet1> snapshots) |
| `VolumeSnapshots` | [`List<Droplet1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet-1.md) | Optional | - | List<Droplet1> getVolumeSnapshots() | setVolumeSnapshots(List<Droplet1> volumeSnapshots) |
| `Volumes` | [`List<Droplet1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet-1.md) | Optional | - | List<Droplet1> getVolumes() | setVolumes(List<Droplet1> volumes) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Droplet1;
import com.digitalocean.api.models.Resources;
import java.io.IOException;
import java.util.Arrays;

Resources resources = new Resources.Builder()
    .floatingIps(Arrays.asList(
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message4")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message4")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message4")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .reservedIps(Arrays.asList(
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message2")
            .id("id0")
            .name("name0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message2")
            .id("id0")
            .name("name0")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .snapshots(Arrays.asList(
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message4")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message4")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message4")
            .id("id2")
            .name("name2")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .volumeSnapshots(Arrays.asList(
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message0")
            .id("id8")
            .name("name8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message0")
            .id("id8")
            .name("name8")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
    .volumes(Arrays.asList(
        new Droplet1.Builder()
            .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .errorMessage("error_message8")
            .id("id6")
            .name("name6")
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



