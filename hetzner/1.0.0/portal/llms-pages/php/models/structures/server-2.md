# Server 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcjI

Configuration for type Server, required if type is `server`

*This model accepts additional fields of type array.*


# Class Name

`Server2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Server | getId(): int | setId(int id): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Server2Builder;
use HetznerCloudApiLib\ApiHelper;

$server2 = Server2Builder::init(
    162
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



