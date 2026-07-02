# Database

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFiYXNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Database`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `clusterName` | `?string` | Optional | The name of the underlying DigitalOcean DBaaS cluster. This is required for production databases. For dev databases, if cluster_name is not set, a new cluster will be provisioned. | getClusterName(): ?string | setClusterName(?string clusterName): void |
| `dbName` | `?string` | Optional | The name of the MySQL or PostgreSQL database to configure. | getDbName(): ?string | setDbName(?string dbName): void |
| `dbUser` | `?string` | Optional | The name of the MySQL or PostgreSQL user to configure. | getDbUser(): ?string | setDbUser(?string dbUser): void |
| `engine` | [`?string(Engine)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/engine.md) | Optional | - MYSQL: MySQL<br>- PG: PostgreSQL<br>- REDIS: Redis<br><br>**Default**: `Engine::UNSET_` | getEngine(): ?string | setEngine(?string engine): void |
| `name` | `string` | Required | The name. Must be unique across all components within the same app.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `32`, *Pattern*: `^[a-z][a-z0-9-]{0,30}[a-z0-9]$` | getName(): string | setName(string name): void |
| `production` | `?bool` | Optional | Whether this is a production or dev database. | getProduction(): ?bool | setProduction(?bool production): void |
| `version` | `?string` | Optional | The version of the database engine | getVersion(): ?string | setVersion(?string version): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\DatabaseBuilder;
use DigitalOceanApiLib\Models\Engine;
use DigitalOceanApiLib\ApiHelper;

$database = DatabaseBuilder::init(
    'prod-db'
)
    ->clusterName('cluster_name')
    ->dbName('my_db')
    ->dbUser('superuser')
    ->engine(Engine::PG)
    ->production(true)
    ->version('12')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



