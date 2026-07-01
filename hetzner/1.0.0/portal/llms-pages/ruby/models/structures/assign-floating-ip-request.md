# Assign Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkFzc2lnbkZsb2F0aW5nSVBSZXF1ZXN0

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `floating_ip_assigned`        | The floating IP is already assigned                           |

*This model accepts additional fields of type Object.*


# Class Name

`AssignFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | `Integer` | Required | ID of the Server the Floating IP shall be assigned to |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
assign_floating_ip_request = AssignFloatingIpRequest.new(
  server: 42,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



