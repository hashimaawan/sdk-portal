# Server Types

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlclR5cGVz

The Server types the Datacenter can handle

*This model accepts additional fields of type Object.*


# Class Name

`ServerTypes`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `available` | `Array[Float]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `available_for_migration` | `Array[Float]` | Required | IDs of Server types that are supported and for which the Datacenter has enough resources left |
| `supported` | `Array[Float]` | Required | IDs of Server types that are supported in the Datacenter |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server_types = ServerTypes.new(
  available: [
    1,
    2,
    3
  ],
  available_for_migration: [
    1,
    2,
    3
  ],
  supported: [
    1,
    2,
    3
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



