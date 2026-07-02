# V2 Droplets Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`V2DropletsActionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Actions` | [`List<Action>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | List<Action> getActions() | setActions(List<Action> actions) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Action;
import com.digitalocean.api.models.Region;
import com.digitalocean.api.models.V2DropletsActionsResponse;
import java.io.IOException;
import java.util.Arrays;

V2DropletsActionsResponse v2DropletsActionsResponse = new V2DropletsActionsResponse.Builder()
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
            .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



