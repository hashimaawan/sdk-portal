# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg

*This model accepts additional fields of type Object.*


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancer = LoadBalancer.new(
  algorithm: Algorithm.new(
    type: Type28::ROUND_ROBIN,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  created: '2016-01-30T23:55:00+00:00',
  id: 42,
  included_traffic: 10000,
  ingoing_traffic: 216,
  labels: {
    'key0' => 'labels2',
    'key1' => 'labels1'
  },
  load_balancer_type: LoadBalancerType.new(
    deprecated: '2016-01-30T23:50:00+00:00',
    description: 'LB11',
    id: 1,
    max_assigned_certificates: 10,
    max_connections: 20000,
    max_services: 5,
    max_targets: 25,
    name: 'lb11',
    prices: [
      Price.new(
        location: 'fsn1',
        price_hourly: PriceHourly.new(
          gross: '1.1900000000000000',
          net: '1.0000000000',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        price_monthly: PriceMonthly.new(
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
  ),
  location: Location.new(
    city: 'Falkenstein',
    country: 'DE',
    description: 'Falkenstein DC Park 1',
    id: 1,
    latitude: 50.47612,
    longitude: 12.370071,
    name: 'fsn1',
    network_zone: 'eu-central',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  name: 'my-resource',
  outgoing_traffic: 42,
  private_net: [
    PrivateNet.new(
      ip: '10.0.0.2',
      network: 4711,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  protection: Protection.new(
    delete: false,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  public_net: PublicNet.new(
    enabled: false,
    ipv4: Ipv4.new(
      dns_ptr: 'lb1.example.com',
      ip: '1.2.3.4',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    ipv6: Ipv6.new(
      dns_ptr: 'lb1.example.com',
      ip: '2001:db8::1',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  services: [
    LoadBalancerService.new(
      destination_port: 80,
      health_check: LoadBalancerServiceHealthCheck.new(
        interval: 15,
        port: 4711,
        protocol: Protocol6::HTTP,
        retries: 3,
        timeout: 10,
        http: Http.new(
          domain: 'domain4',
          path: 'path2',
          response: 'response8',
          status_codes: [
            'status_codes0',
            'status_codes1',
            'status_codes2'
          ],
          tls: false
        )
      ),
      listen_port: 443,
      protocol: Protocol7::HTTPS,
      proxyprotocol: false,
      http: LoadBalancerServiceHttp.new(
        certificates: [
          180
        ],
        cookie_lifetime: 160,
        cookie_name: 'cookie_name6',
        redirect_http: false,
        sticky_sessions: false,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  targets: [
    LoadBalancerTarget.new(
      type: Type29::IP,
      health_status: [
        HealthStatus.new(
          listen_port: 142,
          status: Status30::UNKNOWN,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        HealthStatus.new(
          listen_port: 142,
          status: Status30::UNKNOWN,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      ip: Ip.new(
        ip: 'ip8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      label_selector: LabelSelector7.new(
        selector: 'selector8',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      server: LoadBalancerTargetServer.new(
        id: 14,
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      targets: [
        Target.new(
          health_status: [
            HealthStatus.new(
              listen_port: 142,
              status: Status30::UNKNOWN,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            HealthStatus.new(
              listen_port: 142,
              status: Status30::UNKNOWN,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            )
          ],
          server: Server11.new(
            id: 14,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          type: 'type2',
          use_private_ip: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Target.new(
          health_status: [
            HealthStatus.new(
              listen_port: 142,
              status: Status30::UNKNOWN,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            HealthStatus.new(
              listen_port: 142,
              status: Status30::UNKNOWN,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            )
          ],
          server: Server11.new(
            id: 14,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          type: 'type2',
          use_private_ip: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        Target.new(
          health_status: [
            HealthStatus.new(
              listen_port: 142,
              status: Status30::UNKNOWN,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            ),
            HealthStatus.new(
              listen_port: 142,
              status: Status30::UNKNOWN,
              additional_properties: {
                'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
              }
            )
          ],
          server: Server11.new(
            id: 14,
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          type: 'type2',
          use_private_ip: false,
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
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



