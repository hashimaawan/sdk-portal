# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFiYXNl

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Database`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ClusterName` | `string` | Optional | The name of the underlying DigitalOcean DBaaS cluster. This is required for production databases. For dev databases, if cluster_name is not set, a new cluster will be provisioned. |
| `DbName` | `string` | Optional | The name of the MySQL or PostgreSQL database to configure. |
| `DbUser` | `string` | Optional | The name of the MySQL or PostgreSQL user to configure. |
| `Engine` | [`Engine?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/engine.md) | Optional | - MYSQL: MySQL<br>- PG: PostgreSQL<br>- REDIS: Redis<br><br>**Default**: `Engine.UNSET` |
| `Name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `Production` | `bool?` | Optional | Whether this is a production or dev database. |
| `Version` | `string` | Optional | The version of the database engine |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;

Database database = new Database
{
    Name = "prod-db",
    ClusterName = "cluster_name",
    DbName = "my_db",
    DbUser = "superuser",
    Engine = Engine.Pg,
    Production = true,
    Version = "12",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



