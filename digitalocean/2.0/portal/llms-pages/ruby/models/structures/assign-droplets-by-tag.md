# Assign Droplets by Tag

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwRHJvcGxldHMlMjUyMGJ5JTI1MjBUYWc

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`AssignDropletsByTag`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tag` | `String` | Required | The name of a Droplet tag corresponding to Droplets assigned to the load balancer. |
| `region` | [`Region2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. |
| `algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/algorithm.md) | Optional | This field has been deprecated. You can no longer specify an algorithm for load balancers.<br><br>**Default**: `Algorithm::ROUND_ROBIN` |
| `created_at` | `DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the load balancer was created. |
| `disable_lets_encrypt_dns_records` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether to disable automatic DNS record creation for Let's Encrypt certificates that are added to the load balancer.<br><br>**Default**: `false` |
| `enable_backend_keepalive` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether HTTP keepalive connections are maintained to target Droplets.<br><br>**Default**: `false` |
| `enable_proxy_protocol` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether PROXY Protocol is in use.<br><br>**Default**: `false` |
| `firewall` | [`Firewall1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/firewall-1.md) | Optional | An object specifying allow and deny rules to control traffic to the load balancer. |
| `forwarding_rules` | [`Array[ForwardingRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/forwarding-rule.md) | Required | An array of objects specifying the forwarding rules for a load balancer.<br><br>**Constraints**: *Minimum Items*: `1` |
| `health_check` | [`HealthCheck1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/health-check-1.md) | Optional | An object specifying health check settings for the load balancer. |
| `http_idle_timeout_seconds` | `Integer` | Optional | An integer value which configures the idle timeout for HTTP requests to the target droplets.<br><br>**Default**: `60`<br><br>**Constraints**: `>= 30`, `<= 600` |
| `id` | `UUID \| String` | Optional, Read-only | A unique ID that can be used to identify and reference a load balancer. |
| `ip` | `String` | Optional, Read-only | An attribute containing the public-facing IP address of the load balancer.<br><br>**Constraints**: *Pattern*: `^$\|^((25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)\.){3}(25[0-5]\|2[0-4][0-9]\|[01]?[0-9][0-9]?)$` |
| `name` | `String` | Optional | A human-readable name for a load balancer instance. |
| `project_id` | `String` | Optional | The ID of the project that the load balancer is associated with. If no ID is provided at creation, the load balancer associates with the user's default project. If an invalid project ID is provided, the load balancer will not be created. |
| `redirect_http_to_https` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether HTTP requests to the load balancer on port 80 will be redirected to HTTPS on port 443.<br><br>**Default**: `false` |
| `size` | [`Size2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/size-2.md) | Optional | This field has been replaced by the `size_unit` field for all regions except in AMS2, NYC2, and SFO1. Each available load balancer size now equates to the load balancer having a set number of nodes.<br><br>* `lb-small` = 1 node<br>* `lb-medium` = 3 nodes<br>* `lb-large` = 6 nodes<br><br>You can resize load balancers after creation up to once per hour. You cannot resize a load balancer within the first hour of its creation.<br><br>**Default**: `Size2::LBSMALL` |
| `size_unit` | `Integer` | Optional | How many nodes the load balancer contains. Each additional node increases the load balancer's ability to manage more connections. Load balancers can be scaled up or down, and you can change the number of nodes after creation up to once per hour. This field is currently not available in the AMS2, NYC2, or SFO1 regions. Use the `size` field to scale load balancers that reside in these regions.<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 100` |
| `status` | [`Status12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/status-12.md) | Optional, Read-only | A status string indicating the current state of the load balancer. This can be `new`, `active`, or `errored`. |
| `sticky_sessions` | [`StickySessions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/sticky-sessions.md) | Optional | An object specifying sticky sessions settings for the load balancer. |
| `vpc_uuid` | `UUID \| String` | Optional | A string specifying the UUID of the VPC to which the load balancer is assigned. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
assign_droplets_by_tag = AssignDropletsByTag.new(
  tag: 'prod:web',
  region: Region2::NYC3,
  forwarding_rules: [
    ForwardingRule.new(
      entry_port: 443,
      entry_protocol: EntryProtocol::HTTPS,
      target_port: 80,
      target_protocol: TargetProtocol::HTTP,
      certificate_id: '892071a0-bb95-49bc-8021-3afd67a210bf',
      tls_passthrough: false,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  algorithm: Algorithm::ROUND_ROBIN,
  created_at: DateTimeHelper.from_rfc3339('2017-02-01T22:22:58Z'),
  disable_lets_encrypt_dns_records: true,
  enable_backend_keepalive: true,
  enable_proxy_protocol: true,
  http_idle_timeout_seconds: 90,
  id: '4de7ac8b-495b-4884-9a69-1050c6793cd6',
  ip: '104.131.186.241',
  name: 'example-lb-01',
  project_id: '4de7ac8b-495b-4884-9a69-1050c6793cd6',
  redirect_http_to_https: true,
  size: Size2::LBSMALL,
  size_unit: 3,
  status: Status12::NEW,
  vpc_uuid: 'c33931f2-a26a-4e61-b85c-4e95a2ec431b',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



