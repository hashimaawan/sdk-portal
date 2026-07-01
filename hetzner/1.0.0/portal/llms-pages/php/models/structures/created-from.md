# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from

*This model accepts additional fields of type array.*


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Server the Image was created from | getId(): int | setId(int id): void |
| `name` | `string` | Required | Server name at the time the Image was created | getName(): string | setName(string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreatedFromBuilder;
use HetznerCloudApiLib\ApiHelper;

$createdFrom = CreatedFromBuilder::init(
    1,
    'Server'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



