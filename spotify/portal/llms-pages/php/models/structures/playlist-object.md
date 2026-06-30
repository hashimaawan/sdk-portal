# Playlist Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/php/x-redirect/JTI0bSUyRlBsYXlsaXN0T2JqZWN0

*This model accepts additional fields of type array.*


# Class Name

`PlaylistObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `collaborative` | `?bool` | Optional | `true` if the owner allows other users to modify the playlist. | getCollaborative(): ?bool | setCollaborative(?bool collaborative): void |
| `description` | `?string` | Optional | The playlist description. _Only returned for modified, verified playlists, otherwise_ `null`. | getDescription(): ?string | setDescription(?string description): void |
| `externalUrls` | [`?ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/external-url-object.md) | Optional | Known external URLs for this playlist. | getExternalUrls(): ?ExternalUrlObject | setExternalUrls(?ExternalUrlObject externalUrls): void |
| `followers` | [`?FollowersObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/followers-object.md) | Optional | Information about the followers of the playlist. | getFollowers(): ?FollowersObject | setFollowers(?FollowersObject followers): void |
| `href` | `?string` | Optional | A link to the Web API endpoint providing full details of the playlist. | getHref(): ?string | setHref(?string href): void |
| `id` | `?string` | Optional | The [Spotify ID](/documentation/web-api/concepts/spotify-uris-ids) for the playlist. | getId(): ?string | setId(?string id): void |
| `images` | [`?(ImageObject[])`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/image-object.md) | Optional | Images for the playlist. The array may be empty or contain up to three images. The images are returned by size in descending order. See [Working with Playlists](/documentation/web-api/concepts/playlists). _**Note**: If returned, the source URL for the image (`url`) is temporary and will expire in less than a day._ | getImages(): ?array | setImages(?array images): void |
| `name` | `?string` | Optional | The name of the playlist. | getName(): ?string | setName(?string name): void |
| `owner` | [`?PlaylistOwnerObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/playlist-owner-object.md) | Optional | The user who owns the playlist | getOwner(): ?PlaylistOwnerObject | setOwner(?PlaylistOwnerObject owner): void |
| `public` | `?bool` | Optional | The playlist's public/private status: `true` the playlist is public, `false` the playlist is private, `null` the playlist status is not relevant. For more about public/private status, see [Working with Playlists](/documentation/web-api/concepts/playlists) | getPublic(): ?bool | setPublic(?bool public): void |
| `snapshotId` | `?string` | Optional | The version identifier for the current playlist. Can be supplied in other requests to target a specific playlist version | getSnapshotId(): ?string | setSnapshotId(?string snapshotId): void |
| `tracks` | [`?PagingPlaylistTrackObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/php/models/structures/paging-playlist-track-object.md) | Optional | The tracks of the playlist. | getTracks(): ?PagingPlaylistTrackObject | setTracks(?PagingPlaylistTrackObject tracks): void |
| `type` | `?string` | Optional | The object type: "playlist" | getType(): ?string | setType(?string type): void |
| `uri` | `?string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the playlist. | getUri(): ?string | setUri(?string uri): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PlaylistObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\FollowersObjectBuilder;

$playlistObject = PlaylistObjectBuilder::init()
    ->collaborative(false)
    ->description('description6')
    ->externalUrls(
        ExternalUrlObjectBuilder::init()
            ->spotify('spotify6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->followers(
        FollowersObjectBuilder::init()
            ->href('href0')
            ->total(82)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->href('href6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



