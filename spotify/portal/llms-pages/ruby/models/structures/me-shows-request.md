# Me Shows Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRk1lJTI1MjBTaG93cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`MeShowsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `Array[String]` | Optional | A JSON array of the [Spotify IDs](https://developer.spotify.com/documentation/web-api/#spotify-uris-and-ids).  <br>A maximum of 50 items can be specified in one request. *Note: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored.* |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
me_shows_request = MeShowsRequest.new(
  ids: [
    'ids1',
    'ids2',
    'ids3'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



