# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/java/x-redirect/JTI0bSUyRkRhdGFiYXNl

*This model accepts additional fields of type Object.*


# Class Name

`Database`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ClusterName` | `String` | Optional | The name of the underlying DigitalOcean DBaaS cluster. This is required for production databases. For dev databases, if cluster_name is not set, a new cluster will be provisioned. | String getClusterName() | setClusterName(String clusterName) |
| `DbName` | `String` | Optional | The name of the MySQL or PostgreSQL database to configure. | String getDbName() | setDbName(String dbName) |
| `DbUser` | `String` | Optional | The name of the MySQL or PostgreSQL user to configure. | String getDbUser() | setDbUser(String dbUser) |
| `Engine` | [`Engine`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/java/models/enumerations/engine.md) | Optional | - MYSQL: MySQL<br>- PG: PostgreSQL<br>- REDIS: Redis<br><br>**Default**: `Engine.UNSET` | Engine getEngine() | setEngine(Engine engine) |
| `Name` | `String` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` | String getName() | setName(String name) |
| `Production` | `Boolean` | Optional | Whether this is a production or dev database. | Boolean getProduction() | setProduction(Boolean production) |
| `Version` | `String` | Optional | The version of the database engine | String getVersion() | setVersion(String version) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.digitalocean.api.ApiHelper;
import com.digitalocean.api.models.Database;
import com.digitalocean.api.models.Engine;
import java.io.IOException;

Database database = new Database.Builder(
    "prod-db"
)
.clusterName("cluster_name")
.dbName("my_db")
.dbUser("superuser")
.engine(Engine.PG)
.production(true)
.version("12")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



