# Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vw


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


# Example

```ruby
placement_group = PlacementGroup.new(
  '2016-01-30T23:55:00+00:00',
  42,
  {
    'key0': 'labels4'
  },
  'my-resource',
  [
    42
  ],
  'spread'
)
```



