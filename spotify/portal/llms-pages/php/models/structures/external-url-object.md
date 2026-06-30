# External Url Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRkV4dGVybmFsVXJsT2JqZWN0

*This model accepts additional fields of type array.*


# Class Name

`ExternalUrlObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `spotify` | `?string` | Optional | The [Spotify URL](/documentation/web-api/concepts/spotify-uris-ids) for the object. | getSpotify(): ?string | setSpotify(?string spotify): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$externalUrlObject = ExternalUrlObjectBuilder::init()
    ->spotify('spotify0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



