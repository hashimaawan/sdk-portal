# Add a Server to a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkFkZCUyNTIwYSUyNTIwU2VydmVyJTI1MjB0byUyNTIwYSUyNTIwUGxhY2VtZW50JTI1MjBHcm91cA

Adds a Server to a Placement Group.

Server must be powered off for this command to succeed.

#### Call specific error codes

| Code                          | Description                                                          |
|-------------------------------|----------------------------------------------------------------------|
| `server_not_stopped`          | The action requires a stopped server                                 |

:information_source: **Note** This endpoint does not require authentication.

```csharp
AddAServerToAPlacementGroupAsync(
    int id,
    Models.AddToPlacementGroupRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`AddToPlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/add-to-placement-group-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`Task<Models.ActionResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md)


# Example Usage

```csharp
int id = 112;
AddToPlacementGroupRequest body = new AddToPlacementGroupRequest
{
    PlacementGroup = 1,
};

try
{
    ActionResponse result = await serverActionsController.AddAServerToAPlacementGroupAsync(
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
    "command": "add_to_placement_group",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



