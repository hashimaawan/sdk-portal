# Action Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkFjdGlvblJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`ActionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Required | - | Action getAction() | setAction(Action action) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.ActionResponse;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Status;
import java.io.IOException;
import java.util.Arrays;

ActionResponse actionResponse = new ActionResponse.Builder(
    new Action.Builder(
        "start_server",
        new Error.Builder(
            "action_failed",
            "Action failed"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "2016-01-30T23:55:00+00:00",
        42,
        100D,
        Arrays.asList(
            new Resource.Builder(
                42,
                "server"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "2016-01-30T23:55:00+00:00",
        Status.RUNNING
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



