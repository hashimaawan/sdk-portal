# Namespace

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk5hbWVzcGFjZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`MNamespace`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `apiHost` | `?string` | Optional | The namespace's API hostname. Each function in a namespace is provided an endpoint at the namespace's hostname. | getApiHost(): ?string | setApiHost(?string apiHost): void |
| `createdAt` | `?string` | Optional | UTC time string. | getCreatedAt(): ?string | setCreatedAt(?string createdAt): void |
| `key` | `?string` | Optional | A random alpha numeric string. This key is used in conjunction with the namespace's UUID to authenticate<br>a user to use the namespace via `doctl`, DigitalOcean's official CLI. | getKey(): ?string | setKey(?string key): void |
| `label` | `?string` | Optional | The namespace's unique name. | getLabel(): ?string | setLabel(?string label): void |
| `namespace` | `?string` | Optional | A unique string format of UUID with a prefix fn-. | getNamespace(): ?string | setNamespace(?string namespace): void |
| `region` | `?string` | Optional | The namespace's datacenter region. | getRegion(): ?string | setRegion(?string region): void |
| `updatedAt` | `?string` | Optional | UTC time string. | getUpdatedAt(): ?string | setUpdatedAt(?string updatedAt): void |
| `uuid` | `?string` | Optional | The namespace's Universally Unique Identifier. | getUuid(): ?string | setUuid(?string uuid): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\MNamespaceBuilder;
use DigitalOceanApiLib\ApiHelper;

$namespace = MNamespaceBuilder::init()
    ->apiHost('https://api_host.io')
    ->createdAt('2022-09-14T04:16:45Z')
    ->key('d1zcd455h01mqjfs4s2eaewyejehi5f2uj4etqq3h7cera8iwkub6xg5of1wdde2')
    ->label('my namespace')
    ->namespace('fn-xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx')
    ->region('nyc1')
    ->updatedAt('2022-09-14T04:16:45Z')
    ->uuid('xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



