# V2 Databases Pools Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesPoolsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Db` | `String` | Required | The database for use with the connection pool. | String getDb() | setDb(String db) |
| `Mode` | `String` | Required | The PGBouncer transaction mode for the connection pool. The allowed values are session, transaction, and statement. | String getMode() | setMode(String mode) |
| `Size` | `int` | Required | The desired size of the PGBouncer connection pool. The maximum allowed size is determined by the size of the cluster's primary node. 25 backend server connections are allowed for every 1GB of RAM. Three are reserved for maintenance. For example, a primary node with 1 GB of RAM allows for a maximum of 22 backend server connections while one with 4 GB would allow for 97. Note that these are shared across all connection pools in a cluster. | int getSize() | setSize(int size) |
| `User` | `String` | Optional | The name of the user for use with the connection pool. When excluded, all sessions connect to the database as the inbound user. | String getUser() | setUser(String user) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.V2DatabasesPoolsRequest;
import java.io.IOException;

V2DatabasesPoolsRequest v2DatabasesPoolsRequest = new V2DatabasesPoolsRequest.Builder(
    "defaultdb",
    "transaction",
    10
)
.user("doadmin")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



