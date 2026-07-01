# Load Balancer Type 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU2


# Class Name

`LoadBalancerType6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Float` | Required | ID of the Load Balancer type the price is for |
| `name` | `String` | Required | Name of the Load Balancer type the price is for |
| `prices` | [`Array[Price7]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price-7.md) | Required | Load Balancer type costs per Location |


# Example

```ruby
load_balancer_type6 = LoadBalancerType6.new(
  1,
  'lb11',
  [
    Price7.new(
      'fsn1',
      PriceHourly6.new(
        '1.1900000000000000',
        '1.0000000000'
      ),
      PriceMonthly8.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    )
  ]
)
```



