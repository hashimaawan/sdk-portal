# Delete a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0ZSUyRk5ldHdvcmtzJTJGRGVsZXRlJTI1MjBhJTI1MjBOZXR3b3Jr

Deletes a network. If there are Servers attached they will be detached in the background.

Note: if the network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def delete_a_network(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the network |


# Response Type

**204**: Network deleted

`void`


# Example Usage

```ruby
id = 112

networks_controller.delete_a_network(id)
```



