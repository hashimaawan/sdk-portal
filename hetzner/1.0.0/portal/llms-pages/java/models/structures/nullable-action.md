# Nullable Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRk51bGxhYmxlQWN0aW9u

*This model accepts additional fields of type Object.*


# Class Name

`NullableAction`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Command` | `String` | Required | Command executed in the Action | String getCommand() | setCommand(String command) |
| `Error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null | Error getError() | setError(Error error) |
| `Finished` | `String` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. | String getFinished() | setFinished(String finished) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Progress` | `double` | Required | Progress of Action in percent | double getProgress() | setProgress(double progress) |
| `Resources` | [`List<Resource>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/resource.md) | Required | Resources the Action relates to | List<Resource> getResources() | setResources(List<Resource> resources) |
| `Started` | `String` | Required | Point in time when the Action was started (in ISO-8601 format) | String getStarted() | setStarted(String started) |
| `Status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/enumerations/status.md) | Required | Status of the Action | Status getStatus() | setStatus(Status status) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import cloud.hetzner.api.ApiHelper;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.NullableAction;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.Status;
import java.io.IOException;
import java.util.Arrays;

NullableAction nullableAction = new NullableAction.Builder(
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
.build();
```



