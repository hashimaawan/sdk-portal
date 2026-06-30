# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0


# Class Name

`ChangeIPRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip_range` | `String` | Required | The new prefix for the whole Network |


# Example

```ruby
change_ip_range_request = ChangeIPRangeRequest.new(
  '10.0.0.0/12'
)
```



