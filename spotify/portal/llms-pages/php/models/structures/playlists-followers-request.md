# Playlists Followers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwRm9sbG93ZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`PlaylistsFollowersRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `public` | `?bool` | Optional | Defaults to `true`. If `true` the playlist will be included in user's public playlists, if `false` it will remain private. | getPublic(): ?bool | setPublic(?bool public): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PlaylistsFollowersRequestBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$playlistsFollowersRequest = PlaylistsFollowersRequestBuilder::init()
    ->public(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



