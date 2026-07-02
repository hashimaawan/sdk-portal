# Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk5ldHdvcmtz

The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Networks`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `v_4` | [`Array[V4]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v4.md) | Optional | - |
| `v_6` | [`Array[V6]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v6.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
networks = Networks.new(
  v4: [
    V4.new(
      gateway: 'gateway2',
      ip_address: 'ip_address2',
      netmask: 'netmask2',
      type: Type10::PUBLIC,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    V4.new(
      gateway: 'gateway2',
      ip_address: 'ip_address2',
      netmask: 'netmask2',
      type: Type10::PUBLIC,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    V4.new(
      gateway: 'gateway2',
      ip_address: 'ip_address2',
      netmask: 'netmask2',
      type: Type10::PUBLIC,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  v6: [
    V6.new(
      gateway: 'gateway4',
      ip_address: 'ip_address4',
      netmask: 106,
      type: Type11::PUBLIC,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    V6.new(
      gateway: 'gateway4',
      ip_address: 'ip_address4',
      netmask: 106,
      type: Type11::PUBLIC,
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



