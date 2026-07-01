# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`ChangeDnsptrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dns_ptr` | `String` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` |
| `ip` | `String` | Required | IP address for which to set the reverse DNS entry |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
change_dnsptr_request = ChangeDnsptrRequest.new(
  dns_ptr: 'server02.example.com',
  ip: '1.2.3.4',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



