# Many Genres

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRk1hbnlHZW5yZXM

*This model accepts additional fields of type Object.*


# Class Name

`ManyGenres`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `genres` | `Array[String]` | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
many_genres = ManyGenres.new(
  genres: [
    'alternative',
    'samba'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



