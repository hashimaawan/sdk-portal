# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU


# Class Name

`LoadBalancerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `String` | Required | Point in time when the Load Balancer type is deprecated (in ISO-8601 format) |
| `description` | `String` | Required | Description of the Load Balancer type |
| `id` | `Float` | Required | ID of the Load Balancer type |
| `max_assigned_certificates` | `Float` | Required | Number of SSL Certificates that can be assigned to a single Load Balancer |
| `max_connections` | `Float` | Required | Number of maximum simultaneous open connections |
| `max_services` | `Float` | Required | Number of services a Load Balancer of this type can have |
| `max_targets` | `Float` | Required | Number of targets a single Load Balancer can have |
| `name` | `String` | Required | Unique identifier of the Load Balancer type |
| `prices` | [`Array[Price]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price.md) | Required | Prices in different network zones |


# Example

```ruby
load_balancer_type = LoadBalancerType.new(
  '2016-01-30T23:50:00+00:00',
  'LB11',
  1,
  10,
  20000,
  5,
  25,
  'lb11',
  [
    Price.new(
      'fsn1',
      PriceHourly.new(
        '1.1900000000000000',
        '1.0000000000'
      ),
      PriceMonthly.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    )
  ]
)
```



