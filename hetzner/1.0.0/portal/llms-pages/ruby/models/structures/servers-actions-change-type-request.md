# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server_type` | `String` | Required | ID or name of Server type the Server should migrate to |
| `upgrade_disk` | `TrueClass \| FalseClass` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) |


# Example

```ruby
servers_actions_change_type_request = ServersActionsChangeTypeRequest.new(
  'cx11',
  true
)
```



