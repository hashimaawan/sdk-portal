# Service Dependency

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlNlcnZpY2VEZXBlbmRlbmN5

The state of a registered server dependency.

*This model accepts additional fields of type Object.*


# Class Name

`ServiceDependency`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `String` | Optional | Human-readable message for explaining the current state. |
| `service` | `String` | Optional | - |
| `status` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
service_dependency = ServiceDependency.new(
  message: 'message0',
  service: 'service0',
  status: 'status2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



