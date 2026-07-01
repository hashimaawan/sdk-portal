# Add a Route to a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRk5ldHdvcmslMjUyMEFjdGlvbnMlMkZBZGQlMjUyMGElMjUyMHJvdXRlJTI1MjB0byUyNTIwYSUyNTIwTmV0d29yaw

Adds a route entry to a Network.

Note: if the Network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```csharp
AddARouteToANetworkAsync(
    int id,
    Models.AddDeleteRouteRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Network |
| `body` | [`AddDeleteRouteRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/add-delete-route-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `add_route` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md).


# Example Usage

```csharp
int id = 112;
AddDeleteRouteRequest body = new AddDeleteRouteRequest
{
    Destination = "10.100.1.0/24",
    Gateway = "10.0.1.1",
};

try
{
    ApiResponse<ActionResponse> result = await networkActionsApi.AddARouteToANetworkAsync(
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
    "command": "add_route",
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



