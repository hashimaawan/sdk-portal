# Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlBvb2w

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Pool`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `connection` | [`?Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/connection.md) | Optional | - | getConnection(): ?Connection | setConnection(?Connection connection): void |
| `db` | `string` | Required | The database for use with the connection pool. | getDb(): string | setDb(string db): void |
| `mode` | `string` | Required | The PGBouncer transaction mode for the connection pool. The allowed values are session, transaction, and statement. | getMode(): string | setMode(string mode): void |
| `name` | `string` | Required | A unique name for the connection pool. Must be between 3 and 60 characters. | getName(): string | setName(string name): void |
| `privateConnection` | [`?PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/private-connection.md) | Optional | - | getPrivateConnection(): ?PrivateConnection | setPrivateConnection(?PrivateConnection privateConnection): void |
| `size` | `int` | Required | The desired size of the PGBouncer connection pool. The maximum allowed size is determined by the size of the cluster's primary node. 25 backend server connections are allowed for every 1GB of RAM. Three are reserved for maintenance. For example, a primary node with 1 GB of RAM allows for a maximum of 22 backend server connections while one with 4 GB would allow for 97. Note that these are shared across all connection pools in a cluster. | getSize(): int | setSize(int size): void |
| `user` | `?string` | Optional | The name of the user for use with the connection pool. When excluded, all sessions connect to the database as the inbound user. | getUser(): ?string | setUser(?string user): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\PoolBuilder;
use DigitalOceanApiLib\Models\Builders\ConnectionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\PrivateConnectionBuilder;

$pool = PoolBuilder::init(
    'defaultdb',
    'transaction',
    'backend-pool',
    10
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
    ->user('doadmin')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



