# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA


# Class Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `health_status` | [`Array[HealthStatus]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/health-status.md) | Optional | List of health statuses of the services on this target |
| `ip` | [`Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `label_selector` | [`LabelSelector7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets |
| `server` | [`LoadBalancerTargetServer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through |
| `targets` | [`Array[Target]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/target.md) | Optional | List of selected targets |
| `type` | [`Type29Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-29.md) | Required | Type of the resource |
| `use_private_ip` | `TrueClass \| FalseClass` | Optional | Use the private network IP instead of the public IP. Default value is false. |


# Example

```ruby
load_balancer_target = LoadBalancerTarget.new(
  Type29Enum::SERVER,
  [
    HealthStatus.new(
      142,
      Status30Enum::UNKNOWN
    ),
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
    )
  ]
)
```



