# Create Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`CreatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assignee_id` | `Integer` | Optional | ID of the resource the Primary IP should be assigned to. Omitted if it should not be assigned. |
| `assignee_type` | `String` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` |
| `auto_delete` | `TrueClass \| FalseClass` | Optional | Delete the Primary IP when the Server it is assigned to is deleted. If omitted defaults to `false`. |
| `datacenter` | `String` | Optional | ID or name of Datacenter the Primary IP will be bound to. Needs to be omitted if `assignee_id` is passed. |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | - |
| `type` | [`Type51Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-51.md) | Required | Primary IP type |


# Example

```ruby
create_primary_ip_request = CreatePrimaryIPRequest.new(
  'server',
  'my-ip',
  Type51Enum::IPV4,
  17,
  false,
  'fsn1-dc8',
  { 'labelkey' => 'value' }
)
```



