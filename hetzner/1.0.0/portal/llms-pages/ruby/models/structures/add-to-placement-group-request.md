# Add to Placement Group Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFkZFRvUGxhY2VtZW50R3JvdXBSZXF1ZXN0

*This model accepts additional fields of type Object.*


# Class Name

`AddToPlacementGroupRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `placement_group` | `Integer` | Required | ID of Placement Group the Server should be added to |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
add_to_placement_group_request = AddToPlacementGroupRequest.new(
  placement_group: 1,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



