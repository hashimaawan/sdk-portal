# Private User Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRlByaXZhdGVVc2VyT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`PrivateUserObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Country` | `string` | Optional | The country of the user, as set in the user's account profile. An [ISO 3166-1 alpha-2 country code](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2). _This field is only available when the current user has granted access to the [user-read-private](/documentation/web-api/concepts/scopes/#list-of-scopes) scope._ |
| `DisplayName` | `string` | Optional | The name displayed on the user's profile. `null` if not available. |
| `Email` | `string` | Optional | The user's email address, as entered by the user when creating their account. _**Important!** This email address is unverified; there is no proof that it actually belongs to the user._ _This field is only available when the current user has granted access to the [user-read-email](/documentation/web-api/concepts/scopes/#list-of-scopes) scope._ |
| `ExplicitContent` | [`ExplicitContentSettingsObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/explicit-content-settings-object.md) | Optional | The user's explicit content settings. _This field is only available when the current user has granted access to the [user-read-private](/documentation/web-api/concepts/scopes/#list-of-scopes) scope._ |
| `ExternalUrls` | [`ExternalUrlObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/external-url-object.md) | Optional | Known external URLs for this user. |
| `Followers` | [`FollowersObject`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/followers-object.md) | Optional | Information about the followers of the user. |
| `Href` | `string` | Optional | A link to the Web API endpoint for this user. |
| `Id` | `string` | Optional | The [Spotify user ID](/documentation/web-api/concepts/spotify-uris-ids) for the user. |
| `Images` | [`List<ImageObject>`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/net-standard-library/models/structures/image-object.md) | Optional | The user's profile image. |
| `Product` | `string` | Optional | The user's Spotify subscription level: "premium", "free", etc. (The subscription level "open" can be considered the same as "free".) _This field is only available when the current user has granted access to the [user-read-private](/documentation/web-api/concepts/scopes/#list-of-scopes) scope._ |
| `Type` | `string` | Optional | The object type: "user" |
| `Uri` | `string` | Optional | The [Spotify URI](/documentation/web-api/concepts/spotify-uris-ids) for the user. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

PrivateUserObject privateUserObject = new PrivateUserObject
{
    Country = "country4",
    DisplayName = "display_name0",
    Email = "email6",
    ExplicitContent = new ExplicitContentSettingsObject
    {
        FilterEnabled = false,
        FilterLocked = false,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ExternalUrls = new ExternalUrlObject
    {
        Spotify = "spotify6",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



