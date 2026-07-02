# V2 Actions Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBBY3Rpb25zJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2ActionsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | Action getAction() | setAction(Action action) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Action;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.V2ActionsResponse1;
import java.io.IOException;
import java.util.Arrays;

V2ActionsResponse1 v2ActionsResponse1 = new V2ActionsResponse1.Builder()
    .action(new Action.Builder()
        .completedAt(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
        .id(238)
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
        .regionSlug("region_slug0")
        .resourceId(66)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



