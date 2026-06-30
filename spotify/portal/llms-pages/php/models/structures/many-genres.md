# Many Genres

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRk1hbnlHZW5yZXM

*This model accepts additional fields of type array.*


# Class Name

`ManyGenres`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `genres` | `string[]` | Required | - | getGenres(): array | setGenres(array genres): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ManyGenresBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$manyGenres = ManyGenresBuilder::init(
    [
        'alternative',
        'samba'
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



