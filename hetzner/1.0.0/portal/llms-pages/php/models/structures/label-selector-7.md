# Label Selector 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I3

Label selector and a list of selected targets

*This model accepts additional fields of type array.*


# Class Name

`LabelSelector7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector | getSelector(): string | setSelector(string selector): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LabelSelector7Builder;
use HetznerCloudApiLib\ApiHelper;

$labelSelector7 = LabelSelector7Builder::init(
    'env=prod'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



