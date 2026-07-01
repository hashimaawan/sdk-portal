# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg


# Class Name

`LoadBalancer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/algorithm.md) | Required | Algorithm of the Load Balancer |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `Integer` | Required | ID of the Resource |
| `included_traffic` | `Integer` | Required | Free Traffic for the current billing period in bytes |
| `ingoing_traffic` | `Integer` | Required | Inbound Traffic for the current billing period in bytes |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `load_balancer_type` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-type.md) | Required | - |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/location.md) | Required | - |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `outgoing_traffic` | `Integer` | Required | Outbound Traffic for the current billing period in bytes |
| `private_net` | [`Array[PrivateNet]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/private-net.md) | Required | Private networks information |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `public_net` | [`PublicNet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/public-net.md) | Required | Public network information |
| `services` | [`Array[LoadBalancerService]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-service.md) | Required | List of services that belong to this Load Balancer |
| `targets` | [`Array[LoadBalancerTarget]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-target.md) | Required | List of targets that belong to this Load Balancer |


# Example

```ruby
load_balancer = LoadBalancer.new(
  Algorithm.new(
    Type28Enum::ROUND_ROBIN
  ),
  '2016-01-30T23:55:00+00:00',
  42,
  10000,
  216,
  {
    'key0': 'labels2',
    'key1': 'labels1'
  },
  LoadBalancerType.new(
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
  ),
  Location.new(
    'Falkenstein',
    'DE',
    'Falkenstein DC Park 1',
    1,
    50.47612,
    12.370071,
    'fsn1',
    'eu-central'
  ),
  'my-resource',
  42,
  [
    PrivateNet.new(
      '10.0.0.2',
      4711
    )
  ],
  Protection.new(
    false
  ),
  PublicNet.new(
    false,
    Ipv4.new(
      'lb1.example.com',
      '1.2.3.4'
    ),
    Ipv6.new(
      'lb1.example.com',
      '2001:db8::1'
    )
  ),
  [
    LoadBalancerService.new(
      80,
      LoadBalancerServiceHealthCheck.new(
        15,
        4711,
        Protocol6Enum::HTTP,
        3,
        10,
        Http.new(
          'domain4',
          'path2',
          'response8',
          [
            'status_codes0',
            'status_codes1',
            'status_codes2'
          ],
          false
        )
      ),
      443,
      Protocol7Enum::HTTPS,
      false,
      LoadBalancerServiceHTTP.new(
        [
          180
        ],
        160,
        'cookie_name6',
        false,
        false
      )
    )
  ],
  [
    LoadBalancerTarget.new(
      Type29Enum::IP,
      [
        HealthStatus.new(
          142,
          Status30Enum::UNKNOWN
        ),
        HealthStatus.new(
          142,
          Status30Enum::UNKNOWN
        )
      ],
      Ip.new(
        'ip8'
      ),
      LabelSelector7.new(
        'selector8'
      ),
      LoadBalancerTargetServer.new(
        14
      ),
      [
        Target.new(
          [
            HealthStatus.new(
              142,
              Status30Enum::UNKNOWN
            ),
            HealthStatus.new(
              142,
              Status30Enum::UNKNOWN
            )
          ],
          Server11.new(
            14
          ),
          'type2',
          false
        ),
        Target.new(
          [
            HealthStatus.new(
              142,
              Status30Enum::UNKNOWN
            ),
            HealthStatus.new(
              142,
              Status30Enum::UNKNOWN
            )
          ],
          Server11.new(
            14
          ),
          'type2',
          false
        ),
        Target.new(
          [
            HealthStatus.new(
              142,
              Status30Enum::UNKNOWN
            ),
            HealthStatus.new(
              142,
              Status30Enum::UNKNOWN
            )
          ],
          Server11.new(
            14
          ),
          'type2',
          false
        )
      ]
    )
  ]
)
```



