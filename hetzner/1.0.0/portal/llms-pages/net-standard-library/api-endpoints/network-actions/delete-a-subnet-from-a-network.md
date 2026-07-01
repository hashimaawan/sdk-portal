# Delete a Subnet from a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRk5ldHdvcmslMjUyMEFjdGlvbnMlMkZEZWxldGUlMjUyMGElMjUyMHN1Ym5ldCUyNTIwZnJvbSUyNTIwYSUyNTIwTmV0d29yaw

Deletes a single subnet entry from a Network. You cannot delete subnets which still have Servers attached. If you have Servers attached you first need to detach all Servers that use IPs from this subnet before you can delete the subnet.

Note: if the Network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```csharp
DeleteASubnetFromANetworkAsync(
    int id,
    Models.DeleteSubnetRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Network |
| `body` | [`DeleteSubnetRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/delete-subnet-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `delete_subnet` Action

[`Task<Models.ActionResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md)


# Example Usage

```csharp
int id = 112;
DeleteSubnetRequest body = new DeleteSubnetRequest
{
    IpRange = "10.0.1.0/24",
};

try
{
    ActionResponse result = await networkActionsController.DeleteASubnetFromANetworkAsync(
        id,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
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



