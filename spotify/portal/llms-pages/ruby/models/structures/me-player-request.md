# Me Player Request

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/ruby/x-redirect/JTI0bSUyRk1lJTI1MjBQbGF5ZXIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`MePlayerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `device_ids` | `Array[String]` | Required | A JSON array containing the ID of the device on which playback should be started/transferred.<br/>For example:`{device_ids:["74ASZWbe4lXaubB36ztrGX"]}`<br/>_**Note**: Although an array is accepted, only a single device_id is currently supported. Supplying more than one will return `400 Bad Request`_ |
| `play` | `TrueClass \| FalseClass` | Optional | **true**: ensure playback happens on new device.<br/>**false** or not provided: keep the current playback state. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
me_player_request = MePlayerRequest.new(
  device_ids: [
    '74ASZWbe4lXaubB36ztrGX'
  ],
  play: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



