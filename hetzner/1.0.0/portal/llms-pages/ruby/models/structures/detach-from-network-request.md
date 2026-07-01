# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `Integer` | Required | ID of an existing network to detach the Server from |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
detach_from_network_request = DetachFromNetworkRequest.new(
  network: 4711,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



