# V2 Snapshots Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`V2SnapshotsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Snapshot` | [`Snapshot`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/snapshot.md) | Optional | - | Snapshot getSnapshot() | setSnapshot(Snapshot snapshot) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.ResourceType1;
import com.digitalocean.api.models.Snapshot;
import com.digitalocean.api.models.V2SnapshotsResponse1;
import java.io.IOException;
import java.util.Arrays;

V2SnapshotsResponse1 v2SnapshotsResponse1 = new V2SnapshotsResponse1.Builder()
    .snapshot(new Snapshot.Builder(
        "id8",
        DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
        36,
        "name8",
        Arrays.asList(
            "regions3",
            "regions4",
            "regions5"
        ),
        140.04D,
        "resource_id4",
        ResourceType1.DROPLET,
        Arrays.asList(
            "tags3"
        )
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



