# Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlBvb2w

*This model accepts additional fields of type Object.*


# Class Name

`Pool`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/connection.md) | Optional | - | Connection getConnection() | setConnection(Connection connection) |
| `Db` | `String` | Required | The database for use with the connection pool. | String getDb() | setDb(String db) |
| `Mode` | `String` | Required | The PGBouncer transaction mode for the connection pool. The allowed values are session, transaction, and statement. | String getMode() | setMode(String mode) |
| `Name` | `String` | Required | A unique name for the connection pool. Must be between 3 and 60 characters. | String getName() | setName(String name) |
| `PrivateConnection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/private-connection.md) | Optional | - | PrivateConnection getPrivateConnection() | setPrivateConnection(PrivateConnection privateConnection) |
| `Size` | `int` | Required | The desired size of the PGBouncer connection pool. The maximum allowed size is determined by the size of the cluster's primary node. 25 backend server connections are allowed for every 1GB of RAM. Three are reserved for maintenance. For example, a primary node with 1 GB of RAM allows for a maximum of 22 backend server connections while one with 4 GB would allow for 97. Note that these are shared across all connection pools in a cluster. | int getSize() | setSize(int size) |
| `User` | `String` | Optional | The name of the user for use with the connection pool. When excluded, all sessions connect to the database as the inbound user. | String getUser() | setUser(String user) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Connection;
import com.digitalocean.api.models.Pool;
import com.digitalocean.api.models.PrivateConnection;
import java.io.IOException;

Pool pool = new Pool.Builder(
    "defaultdb",
    "transaction",
    "backend-pool",
    10
)
.connection(new Connection.Builder()
        .database("database2")
        .host("host0")
        .password("password2")
        .port(174)
        .ssl(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.privateConnection(new PrivateConnection.Builder()
        .database("database4")
        .host("host4")
        .password("password8")
        .port(228)
        .ssl(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.user("doadmin")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



