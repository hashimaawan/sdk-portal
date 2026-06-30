# Explicit Content Settings Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/php/x-redirect/JTI0bSUyRkV4cGxpY2l0Q29udGVudFNldHRpbmdzT2JqZWN0

*This model accepts additional fields of type array.*


# Class Name

`ExplicitContentSettingsObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `filterEnabled` | `?bool` | Optional | When `true`, indicates that explicit content should not be played. | getFilterEnabled(): ?bool | setFilterEnabled(?bool filterEnabled): void |
| `filterLocked` | `?bool` | Optional | When `true`, indicates that the explicit content setting is locked and can't be changed by the user. | getFilterLocked(): ?bool | setFilterLocked(?bool filterLocked): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExplicitContentSettingsObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$explicitContentSettingsObject = ExplicitContentSettingsObjectBuilder::init()
    ->filterEnabled(false)
    ->filterLocked(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



