# Floating Ip 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA0

The cost of one Floating IP per month

*This model accepts additional fields of type Object.*


# Class Name

`FloatingIp4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_monthly` | [`PriceMonthly6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-monthly-6.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
floating_ip4 = FloatingIp4.new(
  price_monthly: PriceMonthly6.new(
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
```



