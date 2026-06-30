# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/ruby/x-redirect/JTI0bSUyRlVzZXI

The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more.


# Class Name

`User`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `avatar_url` | `String` | Optional | The URL for this user's avatar image. |
| `banner_url` | `String` | Optional | The URL for the banner image that appears atop this user's profile page. |
| `display_name` | `String` | Optional | The display name associated with this user (contains formatting the base username might not). |
| `profile_url` | `String` | Optional | The URL for this user's profile. |
| `twitter` | `String` | Optional | The Twitter username associated with this user, if applicable. |
| `username` | `String` | Optional | The username associated with this user. |


# Example

```ruby
user = User.new(
  'https://media1.giphy.com/avatars/election2016/XwYrZi5H87o6.gif',
  'https://media4.giphy.com/avatars/cheezburger/XkuejOhoGLE6.jpg',
  'JoeCool4000',
  'https://giphy.com/cheezburger/',
  '@joecool4000',
  'joecool4000'
)
```



