# Paged Categories

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRlBhZ2VkQ2F0ZWdvcmllcw

*This model accepts additional fields of type Any.*


# Class Name

`PagedCategories`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `categories` | [`Categories`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/python/models/structures/categories.md) | Required | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.categories import Categories
from spotifywebapiwithfixesandimprovementsfromsonallux.models.category_object import CategoryObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject
from spotifywebapiwithfixesandimprovementsfromsonallux.models.paged_categories import PagedCategories

paged_categories = PagedCategories(
    categories=Categories(
        href='https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
        limit=20,
        next='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
        offset=0,
        previous='https://api.spotify.com/v1/me/shows?offset=1&limit=1',
        total=4,
        items=[
            CategoryObject(
                href='href0',
                icons=[
                    ImageObject(
                        url='https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
                        height=300,
                        width=300,
                        additional_properties={
                            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                        }
                    )
                ],
                id='equal',
                name='EQUAL',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



