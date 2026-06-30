# Primary Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlByaW1hcnlJcA


# Class Name

`PrimaryIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `prices` | [`Array[Price8]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/price-8.md) | Required | Primary IP type costs per Location |
| `type` | [`Type49Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-49.md) | Required | The type of the Primary IP |


# Example

```ruby
primary_ip = PrimaryIp.new(
  [
    Price8.new(
      'fsn1',
      PriceHourly7.new(
        '1.1900000000000000',
        '1.0000000000'
      ),
      PriceMonthly9.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    )
  ],
  Type49Enum::IPV4
)
```



