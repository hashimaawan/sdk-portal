# Delete a Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZpcmV3YWxscyUyRkRlbGV0ZSUyNTIwYSUyNTIwRmlyZXdhbGw

Deletes a Firewall.

#### Call specific error codes

| Code                 | Description                               |
|--------------------- |-------------------------------------------|
| `resource_in_use`    | Firewall must not be in use to be deleted |

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_firewall(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the resource |


# Response Type

**204**: Firewall deleted

`void`


# Example Usage

```ruby
id = 112

firewalls_controller.delete_a_firewall(id)
```



