# Placement Group Nullable

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwTnVsbGFibGU


# Class Name

`PlacementGroupNullable`


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
placement_group_nullable = PlacementGroupNullable.new(
  '2016-01-30T23:55:00+00:00',
  42,
  {
    'key0': 'labels2',
    'key1': 'labels3',
    'key2': 'labels4'
  },
  'my-resource',
  [
    42
  ],
  'spread'
)
```



