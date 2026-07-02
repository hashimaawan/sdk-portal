# V2 Functions Namespaces Triggers Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlYyJTI1MjBGdW5jdGlvbnMlMjUyME5hbWVzcGFjZXMlMjUyMFRyaWdnZXJzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`V2FunctionsNamespacesTriggersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `function` | `String` | Required | Name of function(action) that exists in the given namespace. |
| `is_enabled` | `TrueClass \| FalseClass` | Required | Indicates weather the trigger is paused or unpaused. |
| `name` | `String` | Required | The trigger's unique name within the namespace. |
| `scheduled_details` | [`ScheduledDetails`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/scheduled-details.md) | Required | Trigger details for SCHEDULED type, where body is optional. |
| `type` | `String` | Required | One of different type of triggers. Currently only SCHEDULED is supported. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
v2_functions_namespaces_triggers_request = V2FunctionsNamespacesTriggersRequest.new(
  function: 'hello',
  is_enabled: true,
  name: 'my trigger',
  scheduled_details: ScheduledDetails.new(
    cron: '* * * * *',
    body: Body.new(
      name: 'name6',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  type: 'SCHEDULED',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



