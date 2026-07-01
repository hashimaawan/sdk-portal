# Create Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVxdWVzdA


# Class Name

`CreatePlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the PlacementGroup |
| `type` | `String` | Required, Constant | Define the Placement Group Type.<br><br>**Value**: `'spread'` |


# Example

```ruby
create_placement_group_request = CreatePlacementGroupRequest.new(
  'my Placement Group',
  'spread',
  { 'key1' => 'val1', 'key2' => 'val2' }
)
```



