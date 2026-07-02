# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGFiYXNl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Database`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cluster_name` | `String` | Optional | The name of the underlying DigitalOcean DBaaS cluster. This is required for production databases. For dev databases, if cluster_name is not set, a new cluster will be provisioned. |
| `db_name` | `String` | Optional | The name of the MySQL or PostgreSQL database to configure. |
| `db_user` | `String` | Optional | The name of the MySQL or PostgreSQL user to configure. |
| `engine` | [`Engine`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/engine.md) | Optional | - MYSQL: MySQL<br>- PG: PostgreSQL<br>- REDIS: Redis<br><br>**Default**: `Engine::UNSET` |
| `name` | `String` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` |
| `production` | `TrueClass \| FalseClass` | Optional | Whether this is a production or dev database. |
| `version` | `String` | Optional | The version of the database engine |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
database = Database.new(
  name: 'prod-db',
  cluster_name: 'cluster_name',
  db_name: 'my_db',
  db_user: 'superuser',
  engine: Engine::PG,
  production: true,
  version: '12',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



