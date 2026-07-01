# Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkVycm9y

Error message for the Action if error occurred, otherwise null

*This model accepts additional fields of type array.*


# Class Name

`Error`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `code` | `string` | Required | Fixed machine readable code | getCode(): string | setCode(string code): void |
| `message` | `string` | Required | Humanized error message | getMessage(): string | setMessage(string message): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ErrorBuilder;
use HetznerCloudApiLib\ApiHelper;

$error = ErrorBuilder::init(
    'action_failed',
    'Action failed'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



