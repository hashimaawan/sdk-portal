# Locations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2U


# Class Name

`LocationsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `locations` | [`Location[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/location.md) | Required | - | getLocations(): array | setLocations(array locations): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LocationsResponseBuilder;
use HetznerCloudAPILib\Models\Builders\LocationBuilder;

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
        )->build()
    ]
)->build();
```



