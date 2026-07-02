# Replica

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlcGxpY2E

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Replica`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `connection` | [`?Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/connection.md) | Optional | - | getConnection(): ?Connection | setConnection(?Connection connection): void |
| `createdAt` | `?DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference a database replica. | getId(): ?string | setId(?string id): void |
| `name` | `string` | Required | The name to give the read-only replicating | getName(): string | setName(string name): void |
| `privateConnection` | [`?PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/private-connection.md) | Optional | - | getPrivateConnection(): ?PrivateConnection | setPrivateConnection(?PrivateConnection privateConnection): void |
| `privateNetworkUuid` | `?string` | Optional | A string specifying the UUID of the VPC to which the read-only replica will be assigned. If excluded, the replica will be assigned to your account's default VPC for the region. | getPrivateNetworkUuid(): ?string | setPrivateNetworkUuid(?string privateNetworkUuid): void |
| `region` | `?string` | Optional | A slug identifier for the region where the read-only replica will be located. If excluded, the replica will be placed in the same region as the cluster. | getRegion(): ?string | setRegion(?string region): void |
| `size` | `?string` | Optional | A slug identifier representing the size of the node for the read-only replica. The size of the replica must be at least as large as the node size for the database cluster from which it is replicating. | getSize(): ?string | setSize(?string size): void |
| `status` | [`?string(Status4)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. | getStatus(): ?string | setStatus(?string status): void |
| `tags` | `?(string[])` | Optional | A flat array of tag names as strings to apply to the read-only replica after it is created. Tag names can either be existing or new tags. | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ReplicaBuilder;
use DigitalOceanApiLib\Models\Builders\ConnectionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\PrivateConnectionBuilder;
use DigitalOceanApiLib\Models\Status4;

$replica = ReplicaBuilder::init(
    'read-nyc3-01'
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
    ->id('9cc10173-e9ea-4176-9dbc-a4cee4c4ff30')
    ->privateConnection(
        PrivateConnectionBuilder::init()
            ->database('database4')
            ->host('host4')
            ->password('password8')
            ->port(228)
            ->ssl(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->privateNetworkUuid('9423cbad-9211-442f-820b-ef6915e99b5f')
    ->region('nyc3')
    ->size('db-s-2vcpu-4gb')
    ->status(Status4::CREATING)
    ->tags(
        [
            'production'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



