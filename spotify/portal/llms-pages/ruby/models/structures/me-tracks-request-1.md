# Me Tracks Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/ruby/x-redirect/JTI0bSUyRk1lJTI1MjBUcmFja3MlMjUyMFJlcXVlc3Qx

*This model accepts additional fields of type Object.*


# Class Name

`MeTracksRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ids` | `Array[String]` | Optional | A JSON array of the [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). For example: `["4iV5W9uYEdYUVa79Axb7Rh", "1301WleyT98MSxVHPZCA6M"]`<br/>A maximum of 50 items can be specified in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
me_tracks_request1 = MeTracksRequest1.new(
  ids: [
    'ids5',
    'ids6'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



