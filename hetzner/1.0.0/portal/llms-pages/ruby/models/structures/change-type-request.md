# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_type` | `String` | Required | ID or name of Load Balancer type the Load Balancer should migrate to |


# Example

```ruby
change_type_request = ChangeTypeRequest.new(
  'lb21'
)
```



