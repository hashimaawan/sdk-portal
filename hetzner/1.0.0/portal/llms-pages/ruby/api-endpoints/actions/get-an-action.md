# Get an Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkFjdGlvbnMlMkZHZXQlMjUyMGFuJTI1MjBBY3Rpb24

Returns a specific Action object.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def get_an_action(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Resource |


# Response Type

**200**: The `action` key in the reply has this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action-response.md)


# Example Usage

```ruby
id = 112

result = actions_controller.get_an_action(id)
puts result
```



