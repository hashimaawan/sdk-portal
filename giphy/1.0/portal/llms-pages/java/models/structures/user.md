# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/java/x-redirect/JTI0bSUyRlVzZXI

The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more.

*This model accepts additional fields of type Object.*


# Class Name

`User`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `AvatarUrl` | `String` | Optional | The URL for this user's avatar image. | String getAvatarUrl() | setAvatarUrl(String avatarUrl) |
| `BannerUrl` | `String` | Optional | The URL for the banner image that appears atop this user's profile page. | String getBannerUrl() | setBannerUrl(String bannerUrl) |
| `DisplayName` | `String` | Optional | The display name associated with this user (contains formatting the base username might not). | String getDisplayName() | setDisplayName(String displayName) |
| `ProfileUrl` | `String` | Optional | The URL for this user's profile. | String getProfileUrl() | setProfileUrl(String profileUrl) |
| `Twitter` | `String` | Optional | The Twitter username associated with this user, if applicable. | String getTwitter() | setTwitter(String twitter) |
| `Username` | `String` | Optional | The username associated with this user. | String getUsername() | setUsername(String username) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.giphy.api.ApiHelper;
import com.giphy.api.models.User;
import java.io.IOException;

User user = new User.Builder()
    .avatarUrl("https://media1.giphy.com/avatars/election2016/XwYrZi5H87o6.gif")
    .bannerUrl("https://media4.giphy.com/avatars/cheezburger/XkuejOhoGLE6.jpg")
    .displayName("JoeCool4000")
    .profileUrl("https://giphy.com/cheezburger/")
    .twitter("@joecool4000")
    .username("joecool4000")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



