# V2 Databases Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`V2DatabasesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/connection.md) | Optional | - | Connection getConnection() | setConnection(Connection connection) |
| `CreatedAt` | `LocalDateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. | LocalDateTime getCreatedAt() | setCreatedAt(LocalDateTime createdAt) |
| `DbNames` | `List<String>` | Optional, Read-only | An array of strings containing the names of databases created in the database cluster. | List<String> getDbNames() | setDbNames(List<String> dbNames) |
| `Engine` | [`Engine1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/engine-1.md) | Required | A slug representing the database engine used for the cluster. The possible values are: "pg" for PostgreSQL, "mysql" for MySQL, "redis" for Redis, and "mongodb" for MongoDB. | Engine1 getEngine() | setEngine(Engine1 engine) |
| `Id` | `UUID` | Optional, Read-only | A unique ID that can be used to identify and reference a database cluster. | UUID getId() | setId(UUID id) |
| `MaintenanceWindow` | [`MaintenanceWindow`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/maintenance-window.md) | Optional | - | MaintenanceWindow getMaintenanceWindow() | setMaintenanceWindow(MaintenanceWindow maintenanceWindow) |
| `Name` | `String` | Required | A unique, human-readable name referring to a database cluster. | String getName() | setName(String name) |
| `NumNodes` | `int` | Required | The number of nodes in the database cluster. | int getNumNodes() | setNumNodes(int numNodes) |
| `PrivateConnection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/private-connection.md) | Optional | - | PrivateConnection getPrivateConnection() | setPrivateConnection(PrivateConnection privateConnection) |
| `PrivateNetworkUuid` | `String` | Optional | A string specifying the UUID of the VPC to which the database cluster will be assigned. If excluded, the cluster when creating a new database cluster, it will be assigned to your account's default VPC for the region.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` | String getPrivateNetworkUuid() | setPrivateNetworkUuid(String privateNetworkUuid) |
| `ProjectId` | `UUID` | Optional | The ID of the project that the database cluster is assigned to. If excluded when creating a new database cluster, it will be assigned to your default project. | UUID getProjectId() | setProjectId(UUID projectId) |
| `Region` | `String` | Required | The slug identifier for the region where the database cluster is located. | String getRegion() | setRegion(String region) |
| `Rules` | [`List<Rule1>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/rule-1.md) | Optional | - | List<Rule1> getRules() | setRules(List<Rule1> rules) |
| `Size` | `String` | Required | The slug identifier representing the size of the nodes in the database cluster. | String getSize() | setSize(String size) |
| `Status` | [`Status4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. | Status4 getStatus() | setStatus(Status4 status) |
| `Tags` | `List<String>` | Optional | An array of tags that have been applied to the database cluster. | List<String> getTags() | setTags(List<String> tags) |
| `Users` | [`List<User>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/user.md) | Optional, Read-only | - | List<User> getUsers() | setUsers(List<User> users) |
| `Version` | `String` | Optional | A string representing the version of the database engine in use for the cluster. | String getVersion() | setVersion(String version) |
| `VersionEndOfAvailability` | `String` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. | String getVersionEndOfAvailability() | setVersionEndOfAvailability(String versionEndOfAvailability) |
| `VersionEndOfLife` | `String` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. | String getVersionEndOfLife() | setVersionEndOfLife(String versionEndOfLife) |
| `BackupRestore` | [`BackupRestore`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/structures/backup-restore.md) | Optional | - | BackupRestore getBackupRestore() | setBackupRestore(BackupRestore backupRestore) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.DateTimeHelper;
import com.digitalocean.api.models.Connection;
import com.digitalocean.api.models.Engine1;
import com.digitalocean.api.models.MaintenanceWindow;
import com.digitalocean.api.models.Status4;
import com.digitalocean.api.models.V2DatabasesRequest;
import java.io.IOException;
import java.util.Arrays;
import java.util.UUID;

V2DatabasesRequest v2DatabasesRequest = new V2DatabasesRequest.Builder(
    Engine1.PG,
    "backend",
    2,
    "nyc3",
    "db-s-2vcpu-4gb"
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
.dbNames(Arrays.asList(
        "doadmin"
    ))
.id(UUID.fromString("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"))
.maintenanceWindow(new MaintenanceWindow.Builder(
        "day0",
        "hour8"
    )
    .description(Arrays.asList(
            "description3",
            "description2"
        ))
    .pending(false)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build())
.privateNetworkUuid("d455e75d-4858-4eec-8c95-da2f0a5f93a7")
.projectId(UUID.fromString("9cc10173-e9ea-4176-9dbc-a4cee4c4ff30"))
.status(Status4.CREATING)
.tags(Arrays.asList(
        "production"
    ))
.version("10")
.versionEndOfAvailability("2023-05-09T00:00:00Z")
.versionEndOfLife("2023-11-09T00:00:00Z")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



