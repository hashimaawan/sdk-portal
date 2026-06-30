# Public User Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRlB1YmxpY1VzZXJPYmplY3Q

*This model accepts additional fields of type array.*


# Class Name

`PublicUserObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `displayName` | `?string` | Optional | The name displayed on the user's profile. `null` if not available. | getDisplayName(): ?string | setDisplayName(?string displayName): void |
| `externalUrls` | [`?ExternalUrlObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/external-url-object.md) | Optional | Known public external URLs for this user. | getExternalUrls(): ?ExternalUrlObject | setExternalUrls(?ExternalUrlObject externalUrls): void |
| `followers` | [`?FollowersObject`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/followers-object.md) | Optional | Information about the followers of this user. | getFollowers(): ?FollowersObject | setFollowers(?FollowersObject followers): void |
| `href` | `?string` | Optional | A link to the Web API endpoint for this user. | getHref(): ?string | setHref(?string href): void |
| `id` | `?string` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for this user. | getId(): ?string | setId(?string id): void |
| `images` | [`?(ImageObject[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/structures/image-object.md) | Optional | The user's profile image. | getImages(): ?array | setImages(?array images): void |
| `type` | [`?string(Type3)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/php/models/enumerations/type-3.md) | Optional | The object type. | getType(): ?string | setType(?string type): void |
| `uri` | `?string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for this user. | getUri(): ?string | setUri(?string uri): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\PublicUserObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\ExternalUrlObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\FollowersObjectBuilder;

$publicUserObject = PublicUserObjectBuilder::init()
    ->displayName('display_name0')
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
    ->href('href2')
    ->id('id0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



