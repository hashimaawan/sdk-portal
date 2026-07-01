# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVzZXI

The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more.

*This model accepts additional fields of type object.*


# Class Name

`User`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AvatarUrl` | `string` | Optional | The URL for this user's avatar image. |
| `BannerUrl` | `string` | Optional | The URL for the banner image that appears atop this user's profile page. |
| `DisplayName` | `string` | Optional | The display name associated with this user (contains formatting the base username might not). |
| `ProfileUrl` | `string` | Optional | The URL for this user's profile. |
| `Twitter` | `string` | Optional | The Twitter username associated with this user, if applicable. |
| `Username` | `string` | Optional | The username associated with this user. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using GiphyApi.Standard.Models;
using GiphyApi.Standard.Utilities;

User user = new User
{
    AvatarUrl = "https://media1.giphy.com/avatars/election2016/XwYrZi5H87o6.gif",
    BannerUrl = "https://media4.giphy.com/avatars/cheezburger/XkuejOhoGLE6.jpg",
    DisplayName = "JoeCool4000",
    ProfileUrl = "https://giphy.com/cheezburger/",
    Twitter = "@joecool4000",
    Username = "joecool4000",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



