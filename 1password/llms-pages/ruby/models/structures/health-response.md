# Health Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRkhlYWx0aCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`HealthResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dependencies` | [`Array[ServiceDependency]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/service-dependency.md) | Optional | - |
| `name` | `String` | Required | - |
| `version` | `String` | Required | The Connect server's version |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
health_response = HealthResponse.new(
  name: 'name6',
  version: 'version2',
  dependencies: [
    ServiceDependency.new(
      message: 'message6',
      service: 'service6',
      status: 'status8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    ServiceDependency.new(
      message: 'message6',
      service: 'service6',
      status: 'status8',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



