# User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/python/x-redirect/JTI0bSUyRlVzZXI

The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more.

*This model accepts additional fields of type Any.*


# Class Name

`User`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `avatar_url` | `str` | Optional | The URL for this user's avatar image. |
| `banner_url` | `str` | Optional | The URL for the banner image that appears atop this user's profile page. |
| `display_name` | `str` | Optional | The display name associated with this user (contains formatting the base username might not). |
| `profile_url` | `str` | Optional | The URL for this user's profile. |
| `twitter` | `str` | Optional | The Twitter username associated with this user, if applicable. |
| `username` | `str` | Optional | The username associated with this user. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from giphyapi.models.user import User

user = User(
    avatar_url='https://media1.giphy.com/avatars/election2016/XwYrZi5H87o6.gif',
    banner_url='https://media4.giphy.com/avatars/cheezburger/XkuejOhoGLE6.jpg',
    display_name='JoeCool4000',
    profile_url='https://giphy.com/cheezburger/',
    twitter='@joecool4000',
    username='joecool4000',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



