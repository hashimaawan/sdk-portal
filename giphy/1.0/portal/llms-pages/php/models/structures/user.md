# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0bSUyRlVzZXI

The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more.

*This model accepts additional fields of type array.*


# Class Name

`User`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `avatarUrl` | `?string` | Optional | The URL for this user's avatar image. | getAvatarUrl(): ?string | setAvatarUrl(?string avatarUrl): void |
| `bannerUrl` | `?string` | Optional | The URL for the banner image that appears atop this user's profile page. | getBannerUrl(): ?string | setBannerUrl(?string bannerUrl): void |
| `displayName` | `?string` | Optional | The display name associated with this user (contains formatting the base username might not). | getDisplayName(): ?string | setDisplayName(?string displayName): void |
| `profileUrl` | `?string` | Optional | The URL for this user's profile. | getProfileUrl(): ?string | setProfileUrl(?string profileUrl): void |
| `twitter` | `?string` | Optional | The Twitter username associated with this user, if applicable. | getTwitter(): ?string | setTwitter(?string twitter): void |
| `username` | `?string` | Optional | The username associated with this user. | getUsername(): ?string | setUsername(?string username): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use GiphyApiLib\Models\Builders\UserBuilder;
use GiphyApiLib\ApiHelper;

$user = UserBuilder::init()
    ->avatarUrl('https://media1.giphy.com/avatars/election2016/XwYrZi5H87o6.gif')
    ->bannerUrl('https://media4.giphy.com/avatars/cheezburger/XkuejOhoGLE6.jpg')
    ->displayName('JoeCool4000')
    ->profileUrl('https://giphy.com/cheezburger/')
    ->twitter('@joecool4000')
    ->username('joecool4000')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



