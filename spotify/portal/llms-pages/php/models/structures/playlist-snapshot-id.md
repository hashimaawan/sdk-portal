# Playlist Snapshot Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRlBsYXlsaXN0U25hcHNob3RJZA

*This model accepts additional fields of type array.*


# Class Name

`PlaylistSnapshotId`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `snapshotId` | `?string` | Optional | - | getSnapshotId(): ?string | setSnapshotId(?string snapshotId): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PlaylistSnapshotIdBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$playlistSnapshotId = PlaylistSnapshotIdBuilder::init()
    ->snapshotId('abc')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



