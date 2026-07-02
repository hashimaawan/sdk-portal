# Database 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFiYXNlMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Database1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `connection` | [`?Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/connection.md) | Optional | - | getConnection(): ?Connection | setConnection(?Connection connection): void |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `dbNames` | `?(string[])` | Optional, Read-only | An array of strings containing the names of databases created in the database cluster. | getDbNames(): ?array | setDbNames(?array dbNames): void |
| `engine` | [`string(Engine1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/engine-1.md) | Required | A slug representing the database engine used for the cluster. The possible values are: "pg" for PostgreSQL, "mysql" for MySQL, "redis" for Redis, and "mongodb" for MongoDB. | getEngine(): string | setEngine(string engine): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference a database cluster. | getId(): ?string | setId(?string id): void |
| `maintenanceWindow` | [`?MaintenanceWindow`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/maintenance-window.md) | Optional | - | getMaintenanceWindow(): ?MaintenanceWindow | setMaintenanceWindow(?MaintenanceWindow maintenanceWindow): void |
| `name` | `string` | Required | A unique, human-readable name referring to a database cluster. | getName(): string | setName(string name): void |
| `numNodes` | `int` | Required | The number of nodes in the database cluster. | getNumNodes(): int | setNumNodes(int numNodes): void |
| `privateConnection` | [`?PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/private-connection.md) | Optional | - | getPrivateConnection(): ?PrivateConnection | setPrivateConnection(?PrivateConnection privateConnection): void |
| `privateNetworkUuid` | `?string` | Optional | A string specifying the UUID of the VPC to which the database cluster will be assigned. If excluded, the cluster when creating a new database cluster, it will be assigned to your account's default VPC for the region.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` | getPrivateNetworkUuid(): ?string | setPrivateNetworkUuid(?string privateNetworkUuid): void |
| `projectId` | `?string` | Optional | The ID of the project that the database cluster is assigned to. If excluded when creating a new database cluster, it will be assigned to your default project. | getProjectId(): ?string | setProjectId(?string projectId): void |
| `region` | `string` | Required | The slug identifier for the region where the database cluster is located. | getRegion(): string | setRegion(string region): void |
| `rules` | [`?(Rule1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/rule-1.md) | Optional | - | getRules(): ?array | setRules(?array rules): void |
| `size` | `string` | Required | The slug identifier representing the size of the nodes in the database cluster. | getSize(): string | setSize(string size): void |
| `status` | [`?string(Status4)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. | getStatus(): ?string | setStatus(?string status): void |
| `tags` | `?(string[])` | Optional | An array of tags that have been applied to the database cluster. | getTags(): ?array | setTags(?array tags): void |
| `users` | [`?(User[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/user.md) | Optional, Read-only | - | getUsers(): ?array | setUsers(?array users): void |
| `version` | `?string` | Optional | A string representing the version of the database engine in use for the cluster. | getVersion(): ?string | setVersion(?string version): void |
| `versionEndOfAvailability` | `?string` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. | getVersionEndOfAvailability(): ?string | setVersionEndOfAvailability(?string versionEndOfAvailability): void |
| `versionEndOfLife` | `?string` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. | getVersionEndOfLife(): ?string | setVersionEndOfLife(?string versionEndOfLife): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Database1Builder;
use DigitalOceanApiLib\Models\Engine1;
use DigitalOceanApiLib\Models\Builders\ConnectionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\MaintenanceWindowBuilder;
use DigitalOceanApiLib\Models\Status4;

$database1 = Database1Builder::init(
    Engine1::PG,
    'backend',
    2,
    'nyc3',
    'db-s-2vcpu-4gb'
)
    ->connection(
        ConnectionBuilder::init()
            ->database('database2')
            ->host('host0')
            ->password('password2')
            ->port(174)
            ->ssl(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2019-01-11T18:37:36Z'))
    ->dbNames(
        [
            'doadmin'
        ]
    )
    ->id('9cc10173-e9ea-4176-9dbc-a4cee4c4ff30')
    ->maintenanceWindow(
        MaintenanceWindowBuilder::init(
            'day0',
            'hour8'
        )
            ->description(
                [
                    'description3',
                    'description2'
                ]
            )
            ->pending(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->privateNetworkUuid('d455e75d-4858-4eec-8c95-da2f0a5f93a7')
    ->projectId('9cc10173-e9ea-4176-9dbc-a4cee4c4ff30')
    ->status(Status4::CREATING)
    ->tags(
        [
            'production'
        ]
    )
    ->version('10')
    ->versionEndOfAvailability('2023-05-09T00:00:00Z')
    ->versionEndOfLife('2023-11-09T00:00:00Z')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



