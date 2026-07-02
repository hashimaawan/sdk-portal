# Mysql Settings

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRk15c3FsU2V0dGluZ3M

*This model accepts additional fields of type Object.*


# Class Name

`MysqlSettings`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AuthPlugin` | [`AuthPlugin`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/auth-plugin.md) | Required | A string specifying the authentication method to be used for connections<br>to the MySQL user account. The valid values are `mysql_native_password`<br>or `caching_sha2_password`. If excluded when creating a new user, the<br>default for the version of MySQL in use will be used. As of MySQL 8.0, the<br>default is `caching_sha2_password`. | AuthPlugin getAuthPlugin() | setAuthPlugin(AuthPlugin authPlugin) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AuthPlugin;
import com.digitalocean.api.models.MysqlSettings;
import java.io.IOException;

MysqlSettings mysqlSettings = new MysqlSettings.Builder(
    AuthPlugin.MYSQL_NATIVE_PASSWORD
)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



