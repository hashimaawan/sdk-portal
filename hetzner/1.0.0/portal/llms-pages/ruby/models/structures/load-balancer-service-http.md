# Load Balancer Service HTTP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIVFRQ

Configuration option for protocols http and https


# Class Name

`LoadBalancerServiceHTTP`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificates` | `Array[Integer]` | Optional | IDs of the Certificates to use for TLS/SSL termination by the Load Balancer; empty for TLS/SSL passthrough or if `protocol` is "http" |
| `cookie_lifetime` | `Integer` | Optional | Lifetime of the cookie used for sticky sessions |
| `cookie_name` | `String` | Optional | Name of the cookie used for sticky sessions |
| `redirect_http` | `TrueClass \| FalseClass` | Optional | Redirect HTTP requests to HTTPS. Only available if protocol is "https". Default `false` |
| `sticky_sessions` | `TrueClass \| FalseClass` | Optional | Use sticky sessions. Only available if protocol is "http" or "https". Default `false` |


# Example

```ruby
load_balancer_service_http = LoadBalancerServiceHTTP.new(
  [
    897
  ],
  300,
  'HCLBSTICKY',
  true,
  true
)
```



