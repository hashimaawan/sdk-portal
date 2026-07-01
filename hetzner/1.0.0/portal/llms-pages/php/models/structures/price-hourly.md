# Price Hourly

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNlSG91cmx5

Hourly costs for a Resource in this Location

*This model accepts additional fields of type array.*


# Class Name

`PriceHourly`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `gross` | `string` | Required | Price with VAT added | getGross(): string | setGross(string gross): void |
| `net` | `string` | Required | Price without VAT | getNet(): string | setNet(string net): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudApiLib\ApiHelper;

$priceHourly = PriceHourlyBuilder::init(
    '1.1900000000000000',
    '1.0000000000'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



