# Destinations

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRlc3RpbmF0aW9ucw

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Destinations`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `addresses` | `Array[String]` | Optional | An array of strings containing the IPv4 addresses, IPv6 addresses, IPv4 CIDRs, and/or IPv6 CIDRs to which the firewall will allow traffic. |
| `droplet_ids` | `Array[Integer]` | Optional | An array containing the IDs of the Droplets to which the firewall will allow traffic. |
| `kubernetes_ids` | `Array[String]` | Optional | An array containing the IDs of the Kubernetes clusters to which the firewall will allow traffic. |
| `load_balancer_uids` | `Array[String]` | Optional | An array containing the IDs of the load balancers to which the firewall will allow traffic. |
| `tags` | `Array[String]` | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
destinations = Destinations.new(
  addresses: [
    '1.2.3.4',
    '18.0.0.0/8'
  ],
  droplet_ids: [
    8043964
  ],
  kubernetes_ids: [
    '41b74c5d-9bd0-5555-5555-a57c495b81a3'
  ],
  load_balancer_uids: [
    '4de7ac8b-495b-4884-9a69-1050c6793cd6'
  ],
  tags: [
    'tags7',
    'tags8',
    'tags9'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



