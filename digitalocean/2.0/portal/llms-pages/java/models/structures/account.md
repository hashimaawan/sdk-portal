# Account

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkFjY291bnQ

*This model accepts additional fields of type Object.*


# Class Name

`Account`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `DropletLimit` | `int` | Required | The total number of Droplets current user or team may have active at one time. | int getDropletLimit() | setDropletLimit(int dropletLimit) |
| `Email` | `String` | Required | The email address used by the current user to register for DigitalOcean. | String getEmail() | setEmail(String email) |
| `EmailVerified` | `boolean` | Required | If true, the user has verified their account via email. False otherwise.<br><br>**Default**: `false` | boolean getEmailVerified() | setEmailVerified(boolean emailVerified) |
| `FloatingIpLimit` | `int` | Required | The total number of Floating IPs the current user or team may have. | int getFloatingIpLimit() | setFloatingIpLimit(int floatingIpLimit) |
| `Status` | [`Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status.md) | Required | This value is one of "active", "warning" or "locked".<br><br>**Default**: `Status.ACTIVE` | Status getStatus() | setStatus(Status status) |
| `StatusMessage` | `String` | Required | A human-readable message giving more details about the status of the account. | String getStatusMessage() | setStatusMessage(String statusMessage) |
| `Team` | [`Team`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/team.md) | Optional | When authorized in a team context, includes information about the current team. | Team getTeam() | setTeam(Team team) |
| `Uuid` | `String` | Required | The unique universal identifier for the current user. | String getUuid() | setUuid(String uuid) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Account;
import com.digitalocean.api.models.Status;
import com.digitalocean.api.models.Team;
import java.io.IOException;

Account account = new Account.Builder(
    25,
    "sammy@digitalocean.com",
    true,
    5,
    Status.ACTIVE,
    " ",
    "b6fr89dbf6d9156cace5f3c78dc9851d957381ef"
)
.team(new Team.Builder()
        .name("name0")
        .uuid("uuid6")
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



