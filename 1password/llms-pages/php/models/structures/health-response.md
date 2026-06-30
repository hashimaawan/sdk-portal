# Health Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRkhlYWx0aCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`HealthResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dependencies` | [`?(ServiceDependency[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/php/models/structures/service-dependency.md) | Optional | - | getDependencies(): ?array | setDependencies(?array dependencies): void |
| `name` | `string` | Required | - | getName(): string | setName(string name): void |
| `version` | `string` | Required | The Connect server's version | getVersion(): string | setVersion(string version): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\HealthResponseBuilder;
use M1PasswordConnectLib\Models\Builders\ServiceDependencyBuilder;
use M1PasswordConnectLib\ApiHelper;

$healthResponse = HealthResponseBuilder::init(
    'name4',
    'version0'
)
    ->dependencies(
        [
            ServiceDependencyBuilder::init()
                ->message('message6')
                ->service('service6')
                ->status('status8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



