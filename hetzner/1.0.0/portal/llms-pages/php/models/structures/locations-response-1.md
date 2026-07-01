# Locations Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type array.*


# Class Name

`LocationsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/location.md) | Required | - | getLocation(): Location | setLocation(Location location): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LocationsResponse1Builder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;

$locationsResponse1 = LocationsResponse1Builder::init(
    LocationBuilder::init(
        'Falkenstein',
        'DE',
        'Falkenstein DC Park 1',
        1,
        50.47612,
        12.370071,
        'fsn1',
        'eu-central'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



