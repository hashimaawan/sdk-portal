# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q


# Class Name

`AssignPrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `Integer` | Required | ID of a resource of type `assignee_type` |
| `assignee_type` | `String` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `'server'` |


# Example

```ruby
assign_primary_ip_request = AssignPrimaryIPRequest.new(
  4711,
  'server'
)
```



