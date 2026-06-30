# API Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkFQSVJlcXVlc3Q

Represents a request that was made to the API. Including what Token was used and what resource was accessed.

*This model accepts additional fields of type Object.*


# Class Name

`ApiRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/action.md) | Optional | - |
| `actor` | [`Actor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/actor.md) | Optional | - |
| `request_id` | `UUID \| String` | Optional | The unique id used to identify a single request. |
| `resource` | [`Resource`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/resource.md) | Optional | - |
| `result` | [`Result`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/enumerations/result.md) | Optional | - |
| `timestamp` | `DateTime` | Optional, Read-only | The time at which the request was processed by the server. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
api_request = ApiRequest.new(
  action: Action::UPDATE,
  actor: Actor.new(
    account: 'account0',
    id: '0000193c-0000-0000-0000-000000000000',
    jti: 'jti2',
    request_ip: 'requestIp4',
    user_agent: 'userAgent6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  request_id: '0000206a-0000-0000-0000-000000000000',
  resource: Resource.new(
    item: Item2.new(
      id: 'id2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    item_version: 108,
    type: Type::ITEM,
    vault: Vault3.new(
      id: 'id6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  result: Result::SUCCESS,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



