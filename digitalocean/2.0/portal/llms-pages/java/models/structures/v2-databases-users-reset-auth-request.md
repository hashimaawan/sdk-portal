# V2 Databases Users Reset Auth Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFVzZXJzJTI1MjBSZXNldCUyNTIwQXV0aCUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesUsersResetAuthRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `MysqlSettings` | [`MysqlSettings`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/mysql-settings.md) | Optional | - | MysqlSettings getMysqlSettings() | setMysqlSettings(MysqlSettings mysqlSettings) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.AuthPlugin;
import com.digitalocean.api.models.MysqlSettings;
import com.digitalocean.api.models.V2DatabasesUsersResetAuthRequest;
import java.io.IOException;

V2DatabasesUsersResetAuthRequest v2DatabasesUsersResetAuthRequest = new V2DatabasesUsersResetAuthRequest.Builder()
    .mysqlSettings(new MysqlSettings.Builder(
        AuthPlugin.MYSQL_NATIVE_PASSWORD
    )
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



