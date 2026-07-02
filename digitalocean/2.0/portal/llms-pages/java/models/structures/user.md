# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlVzZXI

*This model accepts additional fields of type Object.*


# Class Name

`User`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MysqlSettings` | [`MysqlSettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/mysql-settings.md) | Optional | - | MysqlSettings getMysqlSettings() | setMysqlSettings(MysqlSettings mysqlSettings) |
| `Name` | `String` | Required | The name of a database user. | String getName() | setName(String name) |
| `Password` | `String` | Optional, Read-only | A randomly generated password for the database user. | String getPassword() | setPassword(String password) |
| `Role` | [`Role`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/role.md) | Optional, Read-only | A string representing the database user's role. The value will be either<br>"primary" or "normal". | Role getRole() | setRole(Role role) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AuthPlugin;
import com.digitalocean.api.models.MysqlSettings;
import com.digitalocean.api.models.Role;
import com.digitalocean.api.models.User;
import java.io.IOException;

User user = new User.Builder(
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
.build();
```



