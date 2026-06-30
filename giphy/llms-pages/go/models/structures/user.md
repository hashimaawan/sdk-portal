# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/go/x-redirect/JTI0bSUyRlVzZXI

The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more.


# Class Name

`User`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AvatarUrl` | `*string` | Optional | The URL for this user's avatar image. |
| `BannerUrl` | `*string` | Optional | The URL for the banner image that appears atop this user's profile page. |
| `DisplayName` | `*string` | Optional | The display name associated with this user (contains formatting the base username might not). |
| `ProfileUrl` | `*string` | Optional | The URL for this user's profile. |
| `Twitter` | `*string` | Optional | The Twitter username associated with this user, if applicable. |
| `Username` | `*string` | Optional | The username associated with this user. |


# Example

```go
package main

import (
    "giphyapi/models"
)

func main() {
    user := models.User{
        AvatarUrl:            models.ToPointer("https://media1.giphy.com/avatars/election2016/XwYrZi5H87o6.gif"),
        BannerUrl:            models.ToPointer("https://media4.giphy.com/avatars/cheezburger/XkuejOhoGLE6.jpg"),
        DisplayName:          models.ToPointer("JoeCool4000"),
        ProfileUrl:           models.ToPointer("https://giphy.com/cheezburger/"),
        Twitter:              models.ToPointer("@joecool4000"),
        Username:             models.ToPointer("joecool4000"),
    }

}
```



