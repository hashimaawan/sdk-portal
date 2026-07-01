# Load Balancer Type 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU2

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerType6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Float` | Required | ID of the Load Balancer type the price is for |
| `name` | `String` | Required | Name of the Load Balancer type the price is for |
| `prices` | [`Array[Price7]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-7.md) | Required | Load Balancer type costs per Location |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancer_type6 = LoadBalancerType6.new(
  id: 1,
  name: 'lb11',
  prices: [
    Price7.new(
      location: 'fsn1',
      price_hourly: PriceHourly6.new(
        gross: '1.1900000000000000',
        net: '1.0000000000',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      price_monthly: PriceMonthly8.new(
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



