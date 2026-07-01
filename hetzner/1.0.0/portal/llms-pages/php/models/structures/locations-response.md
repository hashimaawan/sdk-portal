# Locations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`LocationsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `locations` | [`Location[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/location.md) | Required | - | getLocations(): array | setLocations(array locations): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LocationsResponseBuilder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;

$locationsResponse = LocationsResponseBuilder::init(
    [
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
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



