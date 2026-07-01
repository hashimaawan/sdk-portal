# Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkZpcmV3YWxsJTI1MjBBY3Rpb25zJTJGUmVtb3ZlJTI1MjBmcm9tJTI1MjBSZXNvdXJjZXM

Removes one Firewall from multiple resources.

Currently only Servers (and their public network interfaces) are supported.

#### Call specific error codes

| Code                                  | Description                                                            |
|---------------------------------------|------------------------------------------------------------------------|
| `firewall_already_removed`            | Firewall was already removed from the resource                         |
| `firewall_resource_not_found`         | The resource the Firewall should be attached to was not found          |
| `firewall_managed_by_label_selector`  | Firewall was applied via label selector and cannot be removed manually |

:information_source: **Note** This endpoint does not require authentication.

```csharp
RemoveFromResourcesAsync(
    int id,
    Models.RemoveFromResourcesRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Firewall |
| `body` | [`RemoveFromResourcesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/remove-from-resources-request.md) | Body, Optional | - |


# Response Type

**201**: The `actions` key contains multiple `remove_firewall` Actions

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ActionsResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/actions-response.md).


# Example Usage

```csharp
int id = 112;
RemoveFromResourcesRequest body = new RemoveFromResourcesRequest
{
    RemoveFrom = new List<FirewallRemoveFromResources>
    {
        new FirewallRemoveFromResources
        {
            Server = new Server9
            {
                Id = 42,
            },
            Type = Type7.Server,
        },
    },
};

try
{
    ApiResponse<ActionsResponse> result = await firewallActionsApi.RemoveFromResourcesAsync(
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
  "actions": [
    {
      "command": "remove_firewall",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 14,
      "progress": 100,
      "resources": [
        {
          "id": 42,
          "type": "server"
        },
        {
          "id": 38,
          "type": "firewall"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



