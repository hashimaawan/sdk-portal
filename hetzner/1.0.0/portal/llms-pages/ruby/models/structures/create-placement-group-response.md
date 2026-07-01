# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/nullable-action.md) | Optional | - |
| `placement_group` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/placement-group.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_placement_group_response = CreatePlacementGroupResponse.new(
  placement_group: PlacementGroup.new(
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
  ),
  action: NullableAction.new(
    command: 'command6',
    error: Error.new(
      code: 'code2',
      message: 'message4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    finished: 'finished0',
    id: 238,
    progress: 143.26,
    resources: [
      Resource.new(
        id: 198,
        type: 'type0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Resource.new(
        id: 198,
        type: 'type0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Resource.new(
        id: 198,
        type: 'type0',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      )
    ],
    started: 'started8',
    status: Status::RUNNING,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



