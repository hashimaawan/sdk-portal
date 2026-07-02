# V2 Volumes Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2VolumesSnapshotsResponse`


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
import com.digitalocean.api.models.V2VolumesSnapshotsResponse;
import java.io.IOException;
import java.util.Arrays;

V2VolumesSnapshotsResponse v2VolumesSnapshotsResponse = new V2VolumesSnapshotsResponse.Builder()
    .snapshot(new Snapshot.Builder(
        "8fa70202-873f-11e6-8b68-000f533176b1",
        DateTimeHelper.fromRfc8601DateTime("2020-09-30T18:56:14Z"),
        10,
        "big-data-snapshot1475261774",
        Arrays.asList(
            "nyc1"
        ),
        10D,
        "82a48a18-873f-11e6-96bf-000f53315a41",
        ResourceType1.VOLUME,
        Arrays.asList(
            "aninterestingtag"
        )
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



