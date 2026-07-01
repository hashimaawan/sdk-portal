# Assign Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFzc2lnblByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`AssignPrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `Integer` | Required | ID of a resource of type `assignee_type` |
| `assignee_type` | `String` | Required, Constant | Type of resource assigning the Primary IP to<br><br>**Value**: `'server'` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
assign_primary_ip_request = AssignPrimaryIpRequest.new(
  assignee_id: 4711,
  assignee_type: 'server',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



