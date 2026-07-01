# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server_types` | [`Array[ServerTypes7]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-types-7.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server_types_response = ServerTypesResponse.new(
  server_types: [
    ServerTypes7.new(
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
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



