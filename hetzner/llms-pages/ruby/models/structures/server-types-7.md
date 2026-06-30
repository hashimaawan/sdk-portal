# Server Types 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzNw


# Class Name

`ServerTypes7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cores` | `Float` | Required | Number of cpu cores a Server of this type will have |
| `cpu_type` | [`CpuTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/cpu-type.md) | Required | Type of cpu |
| `deprecated` | `TrueClass \| FalseClass` | Required | True if Server type is deprecated |
| `description` | `String` | Required | Description of the Server type |
| `disk` | `Float` | Required | Disk size a Server of this type will have in GB |
| `id` | `Float` | Required | ID of the Server type |
| `memory` | `Float` | Required | Memory a Server of this type will have in GB |
| `name` | `String` | Required | Unique identifier of the Server type |
| `prices` | [`Array[Price9]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/price-9.md) | Required | Prices in different Locations |
| `storage_type` | [`StorageTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. |


# Example

```ruby
server_types7 = ServerTypes7.new(
  1,
  CpuTypeEnum::SHARED,
  false,
  'CX11',
  24,
  1,
  1,
  'cx11',
  [
    Price9.new(
      'fsn1',
      PriceHourly8.new(
        '1.1900000000000000',
        '1.0000000000'
      ),
      PriceMonthly10.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    )
  ],
  StorageTypeEnum::LOCAL
)
```



