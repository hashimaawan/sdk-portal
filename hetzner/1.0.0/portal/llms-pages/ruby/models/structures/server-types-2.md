# Server Types 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzMg

*This model accepts additional fields of type Object.*


# Class Name

`ServerTypes2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Float` | Required | ID of the Server type the price is for |
| `name` | `String` | Required | Name of the Server type the price is for |
| `prices` | [`Array[Price9]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-9.md) | Required | Server type costs per Location |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
server_types2 = ServerTypes2.new(
  id: 4,
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
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



