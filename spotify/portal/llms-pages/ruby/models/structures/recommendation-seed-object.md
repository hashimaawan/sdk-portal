# Recommendation Seed Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRlJlY29tbWVuZGF0aW9uU2VlZE9iamVjdA

*This model accepts additional fields of type Object.*


# Class Name

`RecommendationSeedObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `after_filtering_size` | `Integer` | Optional | The number of tracks available after min\_\* and max\_\* filters have been applied. |
| `after_relinking_size` | `Integer` | Optional | The number of tracks available after relinking for regional availability. |
| `href` | `String` | Optional | A link to the full track or artist data for this seed. For tracks this will be a link to a Track Object. For artists a link to an Artist Object. For genre seeds, this value will be `null`. |
| `id` | `String` | Optional | The id used to select this seed. This will be the same as the string used in the `seed_artists`, `seed_tracks` or `seed_genres` parameter. |
| `initial_pool_size` | `Integer` | Optional | The number of recommended tracks available for this seed. |
| `type` | `String` | Optional | The entity type of this seed. One of `artist`, `track` or `genre`. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
recommendation_seed_object = RecommendationSeedObject.new(
  after_filtering_size: 238,
  after_relinking_size: 58,
  href: 'href4',
  id: 'id2',
  initial_pool_size: 244,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



