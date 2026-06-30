# Load Balancers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancers` | [`Array[LoadBalancer]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/load-balancer.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/meta.md) | Optional | - |


# Example

```ruby
load_balancers_response = LoadBalancersResponse.new(
  [
    LoadBalancer.new(
      Algorithm.new(
        Type28Enum::ROUND_ROBIN
      ),
      '2016-01-30T23:55:00+00:00',
      42,
      10000,
      204,
      {
        'key0': 'labels8',
        'key1': 'labels7',
        'key2': 'labels6'
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
      30,
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
  ],
  Meta.new(
    Pagination.new(
      77.7,
      209.18,
      17.58,
      13.34,
      50.02,
      206.64
    )
  )
)
```



