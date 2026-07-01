# Servers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type Object.*


# Class Name

`ServersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
servers_response1 = ServersResponse1.new(
  action: Action.new(
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



