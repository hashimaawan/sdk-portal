# V2 Databases Users Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesUsersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `User` | [`User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/user.md) | Required | - | User getUser() | setUser(User user) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AuthPlugin;
import com.digitalocean.api.models.MysqlSettings;
import com.digitalocean.api.models.Role;
import com.digitalocean.api.models.User;
import com.digitalocean.api.models.V2DatabasesUsersResponse1;
import java.io.IOException;

V2DatabasesUsersResponse1 v2DatabasesUsersResponse1 = new V2DatabasesUsersResponse1.Builder(
    new User.Builder(
        "app-01"
    )
    .mysqlSettings(new MysqlSettings.Builder(
            AuthPlugin.MYSQL_NATIVE_PASSWORD
        )
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .password("jge5lfxtzhx42iff")
    .role(Role.NORMAL)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build()
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



