# Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vw

*This model accepts additional fields of type Object.*


# Class Name

`PlacementGroup`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `Integer` | Required | ID of the Resource |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `servers` | `Array[Integer]` | Required | Array of IDs of Servers that are part of this Placement Group |
| `type` | `String` | Required, Constant | Type of the Placement Group<br><br>**Value**: `'spread'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
placement_group = PlacementGroup.new(
  created: '2016-01-30T23:55:00+00:00',
  id: 42,
  labels: {
    'key0' => 'labels4'
  },
  name: 'my-resource',
  servers: [
    42
  ],
  type: 'spread',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



