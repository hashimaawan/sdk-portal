# Label Selector 12

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3IxMg

Configuration for label selector targets, required if type is `label_selector`

*This model accepts additional fields of type array.*


# Class Name

`LabelSelector12`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector | getSelector(): string | setSelector(string selector): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LabelSelector12Builder;
use HetznerCloudApiLib\ApiHelper;

$labelSelector12 = LabelSelector12Builder::init(
    'env=prod'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



