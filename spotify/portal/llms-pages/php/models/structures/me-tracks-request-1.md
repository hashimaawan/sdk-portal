# Me Tracks Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRk1lJTI1MjBUcmFja3MlMjUyMFJlcXVlc3Qx

*This model accepts additional fields of type array.*


# Class Name

`MeTracksRequest1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ids` | `?(string[])` | Optional | A JSON array of the [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). For example: `["4iV5W9uYEdYUVa79Axb7Rh", "1301WleyT98MSxVHPZCA6M"]`<br/>A maximum of 50 items can be specified in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ | getIds(): ?array | setIds(?array ids): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\MeTracksRequest1Builder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$meTracksRequest1 = MeTracksRequest1Builder::init()
    ->ids(
        [
            'ids3',
            'ids4'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



