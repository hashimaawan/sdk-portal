# V2 Databases Users Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesUsersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Users` | [`List<User>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/user.md) | Optional | - | List<User> getUsers() | setUsers(List<User> users) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AuthPlugin;
import com.digitalocean.api.models.MysqlSettings;
import com.digitalocean.api.models.Role;
import com.digitalocean.api.models.User;
import com.digitalocean.api.models.V2DatabasesUsersResponse;
import java.io.IOException;
import java.util.Arrays;

V2DatabasesUsersResponse v2DatabasesUsersResponse = new V2DatabasesUsersResponse.Builder()
    .users(Arrays.asList(
        new User.Builder(
            "name6"
        )
        .mysqlSettings(new MysqlSettings.Builder(
                AuthPlugin.MYSQL_NATIVE_PASSWORD
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .password("password0")
        .role(Role.PRIMARY)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build(),
        new User.Builder(
            "name6"
        )
        .mysqlSettings(new MysqlSettings.Builder(
                AuthPlugin.MYSQL_NATIVE_PASSWORD
            )
            .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
            .build())
        .password("password0")
        .role(Role.PRIMARY)
        .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build()
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



