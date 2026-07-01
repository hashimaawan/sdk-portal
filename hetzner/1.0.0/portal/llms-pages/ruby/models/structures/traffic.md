# Traffic

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlRyYWZmaWM

The cost of additional traffic per TB

*This model accepts additional fields of type Object.*


# Class Name

`Traffic`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `price_per_tb` | [`PricePerTb`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-per-tb.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
traffic = Traffic.new(
  price_per_tb: PricePerTb.new(
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



