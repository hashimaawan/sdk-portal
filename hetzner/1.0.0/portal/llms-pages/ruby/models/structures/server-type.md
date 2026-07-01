# Server Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlclR5cGU

*This model accepts additional fields of type Object.*


# Class Name

`ServerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cores` | `Float` | Required | Number of cpu cores a Server of this type will have |
| `cpu_type` | [`CpuType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/cpu-type.md) | Required | Type of cpu |
| `deprecated` | `TrueClass \| FalseClass` | Required | True if Server type is deprecated |
| `description` | `String` | Required | Description of the Server type |
| `disk` | `Float` | Required | Disk size a Server of this type will have in GB |
| `id` | `Float` | Required | ID of the Server type |
| `memory` | `Float` | Required | Memory a Server of this type will have in GB |
| `name` | `String` | Required | Unique identifier of the Server type |
| `prices` | [`Array[Price9]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-9.md) | Required | Prices in different Locations |
| `storage_type` | [`StorageType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server_type = ServerType.new(
  cores: 1,
  cpu_type: CpuType::SHARED,
  deprecated: false,
  description: 'CX11',
  disk: 24,
  id: 1,
  memory: 1,
  name: 'cx11',
  prices: [
    Price9.new(
      location: 'fsn1',
      price_hourly: PriceHourly8.new(
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      price_monthly: PriceMonthly10.new(
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  storage_type: StorageType::LOCAL,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



