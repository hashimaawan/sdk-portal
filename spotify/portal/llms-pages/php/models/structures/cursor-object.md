# Cursor Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0bSUyRkN1cnNvck9iamVjdA

*This model accepts additional fields of type array.*


# Class Name

`CursorObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `after` | `?string` | Optional | The cursor to use as key to find the next page of items. | getAfter(): ?string | setAfter(?string after): void |
| `before` | `?string` | Optional | The cursor to use as key to find the previous page of items. | getBefore(): ?string | setBefore(?string before): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\CursorObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$cursorObject = CursorObjectBuilder::init()
    ->after('after0')
    ->before('before8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



