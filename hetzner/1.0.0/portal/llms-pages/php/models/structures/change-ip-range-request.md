# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`ChangeIpRangeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `string` | Required | The new prefix for the whole Network | getIpRange(): string | setIpRange(string ipRange): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ChangeIpRangeRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$changeIpRangeRequest = ChangeIpRangeRequestBuilder::init(
    '10.0.0.0/12'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



