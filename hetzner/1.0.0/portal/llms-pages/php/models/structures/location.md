# Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvY2F0aW9u

*This model accepts additional fields of type array.*


# Class Name

`Location`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `city` | `string` | Required | City the Location is closest to | getCity(): string | setCity(string city): void |
| `country` | `string` | Required | ISO 3166-1 alpha-2 code of the country the Location resides in | getCountry(): string | setCountry(string country): void |
| `description` | `string` | Required | Description of the Location | getDescription(): string | setDescription(string description): void |
| `id` | `float` | Required | ID of the Location | getId(): float | setId(float id): void |
| `latitude` | `float` | Required | Latitude of the city closest to the Location | getLatitude(): float | setLatitude(float latitude): void |
| `longitude` | `float` | Required | Longitude of the city closest to the Location | getLongitude(): float | setLongitude(float longitude): void |
| `name` | `string` | Required | Unique identifier of the Location | getName(): string | setName(string name): void |
| `networkZone` | `string` | Required | Name of network zone this Location resides in | getNetworkZone(): string | setNetworkZone(string networkZone): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;

$location = LocationBuilder::init(
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
    ->build();
```



