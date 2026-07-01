# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaW1hcnlJcA

*This model accepts additional fields of type Object.*


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`Array[Price8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `type` | [`Type49`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-49.md) | Required | The type of the Primary IP |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
primary_ip = PrimaryIp.new(
  prices: [
    Price8.new(
      location: 'fsn1',
      price_hourly: PriceHourly7.new(
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      price_monthly: PriceMonthly9.new(
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
  type: Type49::IPV4,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



