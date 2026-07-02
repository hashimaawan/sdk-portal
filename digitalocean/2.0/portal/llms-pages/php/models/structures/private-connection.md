# Private Connection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlByaXZhdGVDb25uZWN0aW9u

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`PrivateConnection`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `database` | `?string` | Optional, Read-only | The name of the default database. | getDatabase(): ?string | setDatabase(?string database): void |
| `host` | `?string` | Optional, Read-only | The FQDN pointing to the database cluster's current primary node. | getHost(): ?string | setHost(?string host): void |
| `password` | `?string` | Optional, Read-only | The randomly generated password for the default user. | getPassword(): ?string | setPassword(?string password): void |
| `port` | `?int` | Optional, Read-only | The port on which the database cluster is listening. | getPort(): ?int | setPort(?int port): void |
| `ssl` | `?bool` | Optional, Read-only | A boolean value indicating if the connection should be made over SSL. | getSsl(): ?bool | setSsl(?bool ssl): void |
| `uri` | `?string` | Optional, Read-only | A connection string in the format accepted by the `psql` command. This is provided as a convenience and should be able to be constructed by the other attributes. | getUri(): ?string | setUri(?string uri): void |
| `user` | `?string` | Optional, Read-only | The default user for the database. | getUser(): ?string | setUser(?string user): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\PrivateConnectionBuilder;
use DigitalOceanApiLib\ApiHelper;

$privateConnection = PrivateConnectionBuilder::init()
    ->database('defaultdb')
    ->host('backend-do-user-19081923-0.db.ondigitalocean.com')
    ->password('wv78n3zpz42xezdk')
    ->port(25060)
    ->ssl(true)
    ->uri('postgres://doadmin:wv78n3zpz42xezdk@backend-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require')
    ->user('doadmin')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



