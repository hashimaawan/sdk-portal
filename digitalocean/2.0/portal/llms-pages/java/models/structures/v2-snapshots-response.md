# V2 Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`V2SnapshotsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Snapshots` | [`List<Snapshot>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/snapshot.md) | Optional | - | List<Snapshot> getSnapshots() | setSnapshots(List<Snapshot> snapshots) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.ResourceType1;
import com.digitalocean.api.models.Snapshot;
import com.digitalocean.api.models.V2SnapshotsResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2SnapshotsResponse v2SnapshotsResponse = new V2SnapshotsResponse.Builder(
    new Meta.Builder(
        1
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.snapshots(Arrays.asList(
        new Snapshot.Builder(
            "id2",
            DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
            112,
            "name2",
            Arrays.asList(
                "regions7",
                "regions8"
            ),
            148.48D,
            "resource_id8",
            ResourceType1.DROPLET,
            Arrays.asList(
                "tags7",
                "tags8",
                "tags9"
            )
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Snapshot.Builder(
            "id2",
            DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
            112,
            "name2",
            Arrays.asList(
                "regions7",
                "regions8"
            ),
            148.48D,
            "resource_id8",
            ResourceType1.DROPLET,
            Arrays.asList(
                "tags7",
                "tags8",
                "tags9"
            )
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new Snapshot.Builder(
            "id2",
            DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"),
            112,
            "name2",
            Arrays.asList(
                "regions7",
                "regions8"
            ),
            148.48D,
            "resource_id8",
            ResourceType1.DROPLET,
            Arrays.asList(
                "tags7",
                "tags8",
                "tags9"
            )
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.links(new Links.Builder()
        .pages(LinksPages.fromPages(
            new Pages.Builder()
                .last("last6")
                .next("next2")
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
                .build()
        ))
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



