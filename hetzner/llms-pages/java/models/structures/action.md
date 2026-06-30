# Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkFjdGlvbg


# Class Name

`Action`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Command` | `String` | Required | Command executed in the Action | String getCommand() | setCommand(String command) |
| `Error` | [`Error`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null | Error getError() | setError(Error error) |
| `Finished` | `String` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. | String getFinished() | setFinished(String finished) |
| `Id` | `int` | Required | ID of the Resource | int getId() | setId(int id) |
| `Progress` | `double` | Required | Progress of Action in percent | double getProgress() | setProgress(double progress) |
| `Resources` | [`List<Resource>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/resource.md) | Required | Resources the Action relates to | List<Resource> getResources() | setResources(List<Resource> resources) |
| `Started` | `String` | Required | Point in time when the Action was started (in ISO-8601 format) | String getStarted() | setStarted(String started) |
| `Status` | [`StatusEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/enumerations/status.md) | Required | Status of the Action | StatusEnum getStatus() | setStatus(StatusEnum status) |


# Example

```java
import cloud.hetzner.api.models.Action;
import cloud.hetzner.api.models.Error;
import cloud.hetzner.api.models.Resource;
import cloud.hetzner.api.models.StatusEnum;
import java.util.Arrays;

Action action = new Action.Builder(
    "start_server",
    new Error.Builder(
        "action_failed",
        "Action failed"
    )
    .build(),
    "2016-01-30T23:55:00+00:00",
    42,
    100D,
    Arrays.asList(
        new Resource.Builder(
            42,
            "server"
        )
        .build()
    ),
    "2016-01-30T23:55:00+00:00",
    StatusEnum.RUNNING
)
.build();
```



