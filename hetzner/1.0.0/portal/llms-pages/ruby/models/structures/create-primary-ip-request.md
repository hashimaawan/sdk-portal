# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`CreatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `Integer` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. |
| `assignee_type` | `String` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` |
| `auto_delete` | `TrueClass \| FalseClass` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. |
| `datacenter` | `String` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | - |
| `type` | [`Type51`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-51.md) | Required | Primary IP type |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_primary_ip_request = CreatePrimaryIpRequest.new(
  assignee_type: 'server',
  name: 'my-ip',
  type: Type51::IPV4,
  assignee_id: 17,
  auto_delete: false,
  datacenter: 'fsn1-dc8',
  labels: { 'labelkey' => 'value' },
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



