# Labels 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxhYmVsczI

User-defined labels (key-value pairs)

*This model accepts additional fields of type array.*


# Class Name

`Labels2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labelkey` | `?string` | Optional | - | getLabelkey(): ?string | setLabelkey(?string labelkey): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\Labels2Builder;
use HetznerCloudApiLib\ApiHelper;

$labels2 = Labels2Builder::init()
    ->labelkey('value')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



