# Service Dependency

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/php/x-redirect/JTI0bSUyRlNlcnZpY2VEZXBlbmRlbmN5

The state of a registered server dependency.

*This model accepts additional fields of type array.*


# Class Name

`ServiceDependency`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `message` | `?string` | Optional | Human-readable message for explaining the current state. | getMessage(): ?string | setMessage(?string message): void |
| `service` | `?string` | Optional | - | getService(): ?string | setService(?string service): void |
| `status` | `?string` | Optional | - | getStatus(): ?string | setStatus(?string status): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use M1PasswordConnectLib\Models\Builders\ServiceDependencyBuilder;
use M1PasswordConnectLib\ApiHelper;

$serviceDependency = ServiceDependencyBuilder::init()
    ->message('message6')
    ->service('service6')
    ->status('status8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



