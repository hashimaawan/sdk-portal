# Recommendation Seed Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/python/x-redirect/JTI0bSUyRlJlY29tbWVuZGF0aW9uU2VlZE9iamVjdA

*This model accepts additional fields of type Any.*


# Class Name

`RecommendationSeedObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `after_filtering_size` | `int` | Optional | The number of tracks available after min\_\* and max\_\* filters have been applied. |
| `after_relinking_size` | `int` | Optional | The number of tracks available after relinking for regional availability. |
| `href` | `str` | Optional | A link to the full track or artist data for this seed. For tracks this will be a link to a Track Object. For artists a link to an Artist Object. For genre seeds, this value will be `null`. |
| `id` | `str` | Optional | The id used to select this seed. This will be the same as the string used in the `seed_artists`, `seed_tracks` or `seed_genres` parameter. |
| `initial_pool_size` | `int` | Optional | The number of recommended tracks available for this seed. |
| `mtype` | `str` | Optional | The entity type of this seed. One of `artist`, `track` or `genre`. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.recommendation_seed_object import RecommendationSeedObject

recommendation_seed_object = RecommendationSeedObject(
    after_filtering_size=238,
    after_relinking_size=58,
    href='href4',
    id='id2',
    initial_pool_size=244,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



