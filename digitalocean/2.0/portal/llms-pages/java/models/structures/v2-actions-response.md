# V2 Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2ActionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | List<Action> getActions() | setActions(List<Action> actions) |
| `Links` | [`Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/links.md) | Optional | - | Links getLinks() | setLinks(Links links) |
| `Meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/meta.md) | Required | - | Meta getMeta() | setMeta(Meta meta) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Action;
import com.digitalocean.api.models.Links;
import com.digitalocean.api.models.Meta;
import com.digitalocean.api.models.Pages;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.V2ActionsResponse;
import com.digitalocean.api.models.containers.LinksPages;
import java.io.IOException;
import java.util.Arrays;

V2ActionsResponse v2ActionsResponse = new V2ActionsResponse.Builder(
    new Meta.Builder(
        1
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.actions(Arrays.asList(
        new Action.Builder()
            .completedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .id(154)
            .region(new Region.Builder(
                false,
                Arrays.asList(
                    "features7",
                    "features8",
                    "features9"
                ),
                "name6",
                Arrays.asList(
                    "sizes6"
                ),
                "slug0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .regionSlug("region_slug6")
            .resourceId(238)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Action.Builder()
            .completedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .id(154)
            .region(new Region.Builder(
                false,
                Arrays.asList(
                    "features7",
                    "features8",
                    "features9"
                ),
                "name6",
                Arrays.asList(
                    "sizes6"
                ),
                "slug0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .regionSlug("region_slug6")
            .resourceId(238)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
        new Action.Builder()
            .completedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
            .id(154)
            .region(new Region.Builder(
                false,
                Arrays.asList(
                    "features7",
                    "features8",
                    "features9"
                ),
                "name6",
                Arrays.asList(
                    "sizes6"
                ),
                "slug0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
            .regionSlug("region_slug6")
            .resourceId(238)
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



