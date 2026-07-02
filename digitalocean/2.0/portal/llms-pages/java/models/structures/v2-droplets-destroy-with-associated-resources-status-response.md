# V2 Droplets Destroy with Associated Resources Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTdGF0dXMlMjUyMFJlc3BvbnNl

An objects containing information about a resources scheduled for deletion.

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesStatusResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CompletedAt` | `LocalDateTime` | Optional | A time value given in ISO8601 combined date and time format indicating when the requested action was completed. | LocalDateTime getCompletedAt() | setCompletedAt(LocalDateTime completedAt) |
| `Droplet` | [`Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/droplet-1.md) | Optional | An object containing information about a resource scheduled for deletion. | Droplet1 getDroplet() | setDroplet(Droplet1 droplet) |
| `Failures` | `Integer` | Optional | A count of the associated resources that failed to be destroyed, if any. | Integer getFailures() | setFailures(Integer failures) |
| `Resources` | [`Resources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/resources.md) | Optional | An object containing additional information about resource related to a Droplet requested to be destroyed. | Resources getResources() | setResources(Resources resources) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Droplet1;
import com.digitalocean.api.models.Resources;
import com.digitalocean.api.models.V2DropletsDestroyWithAssociatedResourcesStatusResponse;
import java.io.IOException;
import java.util.Arrays;

V2DropletsDestroyWithAssociatedResourcesStatusResponse v2DropletsDestroyWithAssociatedResourcesStatusResponse = new V2DropletsDestroyWithAssociatedResourcesStatusResponse.Builder()
    .completedAt(DateTimeHelper.fromRfc8601DateTime("2020-04-01T18:11:49Z"))
    .droplet(new Droplet1.Builder()
        .destroyedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .errorMessage("error_message2")
        .id("id0")
        .name("name0")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .failures(0)
    .resources(new Resources.Builder()
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
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



