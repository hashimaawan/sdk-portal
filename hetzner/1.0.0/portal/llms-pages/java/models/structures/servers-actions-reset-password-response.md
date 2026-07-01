# Servers Actions Reset Password Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlc2V0JTI1MjBQYXNzd29yZCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`ServersActionsResetPasswordResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action.md) | Optional | - | Action getAction() | setAction(Action action) |
| `RootPassword` | `String` | Optional | Password that will be set for this Server once the Action succeeds | String getRootPassword() | setRootPassword(String rootPassword) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.ServersActionsResetPasswordResponse;
import cloud.hetzner.api.models.Status;
import java.io.IOException;
import java.util.Arrays;

ServersActionsResetPasswordResponse serversActionsResetPasswordResponse = new ServersActionsResetPasswordResponse.Builder()
    .action(new Action.Builder(
        "command6",
        new Error.Builder(
            "code2",
            "message4"
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        "finished0",
        238,
        143.26D,
        Arrays.asList(
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build(),
            new Resource.Builder(
                198,
                "type0"
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build()
        ),
        "started8",
        Status.RUNNING
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
    .rootPassword("zCWbFhnu950dUTko5f40")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



