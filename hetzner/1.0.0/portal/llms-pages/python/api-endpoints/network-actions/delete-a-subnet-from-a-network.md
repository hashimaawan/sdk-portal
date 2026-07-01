# Delete a Subnet from a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRk5ldHdvcmslMjUyMEFjdGlvbnMlMkZEZWxldGUlMjUyMGElMjUyMHN1Ym5ldCUyNTIwZnJvbSUyNTIwYSUyNTIwTmV0d29yaw

Deletes a single subnet entry from a Network. You cannot delete subnets which still have Servers attached. If you have Servers attached you first need to detach all Servers that use IPs from this subnet before you can delete the subnet.

Note: if the Network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_a_subnet_from_a_network(self,
                                  id,
                                  body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Network |
| `body` | [`DeleteSubnetRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/delete-subnet-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `delete_subnet` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md).


# Example Usage

```python
id = 112

body = DeleteSubnetRequest(
    ip_range='10.0.1.0/24'
)

result = network_actions_api.delete_a_subnet_from_a_network(
    id,
    body=body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "delete_subnet",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 4711,
        "type": "network"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



