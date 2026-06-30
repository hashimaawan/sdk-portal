# Followers Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRkZvbGxvd2Vyc09iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`FollowersObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Optional | This will always be set to null, as the Web API does not support it at the moment. |
| `total` | `int` | Optional | The total number of followers. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.followers_object import FollowersObject

followers_object = FollowersObject(
    href='href8',
    total=198,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



