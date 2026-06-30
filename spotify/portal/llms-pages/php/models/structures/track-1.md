# Track 1

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0bSUyRlRyYWNrMQ

*This model accepts additional fields of type array.*


# Class Name

`Track1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `uri` | `?string` | Optional | Spotify URI | getUri(): ?string | setUri(?string uri): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\Track1Builder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$track1 = Track1Builder::init()
    ->uri('uri0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



