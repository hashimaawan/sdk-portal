# Replica

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlJlcGxpY2E

*This model accepts additional fields of type Object.*


# Class Name

`Replica`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/connection.md) | Optional | - | Connection getConnection() | setConnection(Connection connection) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `Id` | `UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a database replica. | UUID getId() | setId(UUID id) |
| `Name` | `String` | Required | The name to give the read-only replicating | String getName() | setName(String name) |
| `PrivateConnection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/private-connection.md) | Optional | - | PrivateConnection getPrivateConnection() | setPrivateConnection(PrivateConnection privateConnection) |
| `PrivateNetworkUuid` | `String` | Optional | A string specifying the UUID of the VPC to which the read-only replica will be assigned. If excluded, the replica will be assigned to your account's default VPC for the region. | String getPrivateNetworkUuid() | setPrivateNetworkUuid(String privateNetworkUuid) |
| `Region` | `String` | Optional | A slug identifier for the region where the read-only replica will be located. If excluded, the replica will be placed in the same region as the cluster. | String getRegion() | setRegion(String region) |
| `Size` | `String` | Optional | A slug identifier representing the size of the node for the read-only replica. The size of the replica must be at least as large as the node size for the database cluster from which it is replicating. | String getSize() | setSize(String size) |
| `Status` | [`Status4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. | Status4 getStatus() | setStatus(Status4 status) |
| `Tags` | `List<String>` | Optional | A flat array of tag names as strings to apply to the read-only replica after it is created. Tag names can either be existing or new tags. | List<String> getTags() | setTags(List<String> tags) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Connection;
import com.digitalocean.api.models.PrivateConnection;
import com.digitalocean.api.models.Replica;
import com.digitalocean.api.models.Status4;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

Replica replica = new Replica.Builder(
    "read-nyc3-01"
)
.connection(new Connection.Builder()
        .database("database2")
        .host("host0")
        .password("password2")
        .port(174)
        .ssl(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.createdAt(DateTimeHelper.fromRfc8601DateTime("2019-01-11T18:37:36Z"))
.id(UUID.fromString("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"))
.privateConnection(new PrivateConnection.Builder()
        .database("database4")
        .host("host4")
        .password("password8")
        .port(228)
        .ssl(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.privateNetworkUuid("9423cbad-9211-442f-820b-ef6915e99b5f")
.region("nyc3")
.size("db-s-2vcpu-4gb")
.status(Status4.CREATING)
.tags(Arrays.asList(
        "production"
    ))
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



