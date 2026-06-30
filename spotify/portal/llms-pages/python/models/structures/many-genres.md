# Many Genres

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRk1hbnlHZW5yZXM

*This model accepts additional fields of type Any.*


# Class Name

`ManyGenres`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `genres` | `List[str]` | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.many_genres import ManyGenres

many_genres = ManyGenres(
    genres=[
        'alternative',
        'samba'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



