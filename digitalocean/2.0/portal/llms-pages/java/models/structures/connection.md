# Connection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkNvbm5lY3Rpb24

*This model accepts additional fields of type Object.*


# Class Name

`Connection`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Database` | `String` | Optional, Read-only | The name of the default database. | String getDatabase() | setDatabase(String database) |
| `Host` | `String` | Optional, Read-only | The FQDN pointing to the database cluster's current primary node. | String getHost() | setHost(String host) |
| `Password` | `String` | Optional, Read-only | The randomly generated password for the default user. | String getPassword() | setPassword(String password) |
| `Port` | `Integer` | Optional, Read-only | The port on which the database cluster is listening. | Integer getPort() | setPort(Integer port) |
| `Ssl` | `Boolean` | Optional, Read-only | A boolean value indicating if the connection should be made over SSL. | Boolean getSsl() | setSsl(Boolean ssl) |
| `Uri` | `String` | Optional, Read-only | A connection string in the format accepted by the `psql` command. This is provided as a convenience and should be able to be constructed by the other attributes. | String getUri() | setUri(String uri) |
| `User` | `String` | Optional, Read-only | The default user for the database. | String getUser() | setUser(String user) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Connection;
import java.io.IOException;

Connection connection = new Connection.Builder()
    .database("defaultdb")
    .host("backend-do-user-19081923-0.db.ondigitalocean.com")
    .password("wv78n3zpz42xezdk")
    .port(25060)
    .ssl(true)
    .uri("postgres://doadmin:wv78n3zpz42xezdk@backend-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require")
    .user("doadmin")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



