# Update a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZVcGRhdGUlMjUyMGElMjUyMFNlcnZlcg

Updates a Server. You can update a Server’s name and a Server’s labels.
Please note that Server names must be unique per Project and valid hostnames as per RFC 1123 (i.e. may only contain letters, digits, periods, and dashes).
Also note that when updating labels, the Server’s current set of labels will be replaced with the labels provided in the request body. So, for example, if you want to add a new label, you have to provide all existing labels plus the new label in the request body.

:information_source: **Note** This endpoint does not require authentication.

```python
def update_a_server(self,
                   id,
                   body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`UpdateServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/update-server-request.md) | Body, Optional | - |


# Response Type

**200**: The `server` key in the reply contains the updated Server

[`ServersResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/servers-response-2.md)


# Example Usage

```python
id = 112

body = UpdateServerRequest(
    labels=jsonpickle.decode('{"labelkey":"value"}'),
    name='my-server'
)

result = servers_controller.update_a_server(
    id,
    body=body
)
print(result)
```



